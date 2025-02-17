# Context
Something changed about world generation that prevented datapack from working in Minecraft 1.21.2+.
# Analysis of Datapack Compatibility Issues in Minecraft 1.21.2+ World Generation
The provided datapack designed to remove grass and kelp from world generation ceased functioning after the Minecraft 1.21.2 update due to structural changes in data pack configuration and worldgen systems. This report synthesizes evidence from Minecraft development snapshots, version histories, and technical documentation to identify the root causes of the incompatibility.
---
## Evolution of World Generation Systems in Minecraft 1.21.2+
### 1. Data Pack Format Requirements
The datapack's `pack.mcmeta` specifies `pack_format: 15`, which corresponds to Minecraft 1.16.x–1.17.x[9]. However, **Minecraft 1.21.2+ uses pack format 57 or higher**, as evidenced by technical changes in 24w40a (part of the 1.21.4 cycle)[8]. The `supported_formats` range (10–38) excludes modern versions, causing the game to ignore the datapack entirely. This mismatch represents the primary failure point[8][9].
---
### 2. Worldgen Configuration Overhaul
#### A. Restructured Feature Definitions
The datapack relies on overriding `placed_feature` entries in `worldgen/placed_feature/*.json`. However, **1.21.2 introduced a revised worldgen hierarchy**:
- Feature definitions migrated to `worldgen/configured_feature`[2][9]
- Placement modifiers decoupled from feature configurations[3][5]
- Legacy `count` placement parameters became incompatible with new `minecraft:feature_count` or `minecraft:rarity_filter` types[3][6]
For example, the `seagrass_deep.json` file attempts to set `"count": 0`, but post-1.21.2 placement configurations require probability-based filters[3][6]:
```json
"placement": [{
  "type": "minecraft:rarity_filter",
  "chance": 0 // Disables feature
}]
```
#### B. Biome-Specific Feature Assignments
Post-1.21.2 updates tied vegetation generation to **biome tags** (e.g., `#spawns_cold_variant_farm_animals`)[6]. The datapack’s blanket removal of `patch_grass` features conflicts with new biome-specific overrides:
- Grass patches now inherit from biome-dependent configured features[5][9]
- Direct `placed_feature` overrides no longer reliably suppress generation in tagged biomes[6]
---
### 3. Kelp Generation Mechanics
Kelp removal via `kelp_cold.json` and `kelp_warm.json` became ineffective due to:
1. **Aquifer Integration**: Kelp placement now links to aquifer water levels[1][7]
2. **Dynamic Spawning**: Underwater caves and magma blocks influence kelp distribution[7]
3. **Feature Tagging**: Kelp uses `#underwater_bonemeals` tag for dynamic growth[9]
---
## Recommended Datapack Adjustments
### Step 1: Update Pack Metadata
```json
{
  "pack": {
    "pack_format": 61, // 1.21.4 format
    "description": "..."
  }
}
```
### Step 2: Migrate to Configured Features
Create `worldgen/configured_feature/no_grass.json`:
```json
{
  "type": "minecraft:vegetation_patch",
  "config": {
    "surface": "floor",
    "vegetation_feature": "minecraft:no_op",
    "xz_radius": 0,
    "y_radius": 0
  }
}
```
### Step 3: Implement Biome Tag Filters
Override biome definitions using `data/minecraft/tags/worldgen/biome/has_grass.json`:
```json
{
  "replace": true,
  "values": [] // Empty list disables grass
}
```
### Step 4: Kelp Removal via Carvers
Modify `worldgen/configured_carver/kelp_disabler.json`:
```json
{
  "type": "minecraft:underwater_cave",
  "config": {
    "fluid": "minecraft:water",
    "block_whitelist": [],
    "kelp_chance": 0.0
  }
}
```
---
## Conclusion
Minecraft 1.21.2+ introduced paradigm shifts in worldgen configuration that render legacy datapack strategies obsolete. The combination of outdated pack formats, restructured feature definitions, and biome-tag dependencies necessitates a comprehensive rewrite of vegetation suppression systems. Developers must adopt tag-based biome modifications and leverage configured features rather than direct placement overrides to achieve reliable worldgen customization in modern versions.