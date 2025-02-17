# Codebase:
## Folder Contents:
### Folder structure:
```
NoMoreGrassAndKelp/
├── data/
│   └── minecraft/
│       └── worldgen/
│           └── placed_feature/
│               ├── seagrass_cold.json
│               ├── seagrass_deep.json
│               ├── seagrass_deep_cold.json
│               ├── seagrass_deep_warm.json
│               ├── seagrass_normal.json
│               ├── seagrass_river.json
│               ├── patch_grass_taiga_2.json
│               ├── patch_large_fern.json
│               ├── patch_taiga_grass.json
│               ├── patch_tall_grass.json
│               ├── patch_tall_grass_2.json
│               ├── patch_grass_badlands.json
│               ├── patch_grass_forest.json
│               ├── patch_grass_jungle.json
│               ├── patch_grass_normal.json
│               ├── patch_grass_plain.json
│               ├── patch_grass_savanna.json
│               ├── patch_grass_taiga.json
│               ├── seagrass_simple.json
│               ├── seagrass_swamp.json
│               ├── seagrass_warm.json
│               ├── disk_grass.json
│               ├── kelp_cold.json
│               └── kelp_warm.json
├── pack.png
└── pack.mcmeta
```
## File Contents:
### `pack.mcmeta`:
```mcmeta
{
  "pack": {
    "pack_format": 15,
    "supported_formats": {
      "min_inclusive": 10,
      "max_inclusive": 38
    },
    "description": "Removes grass, tall grass, kelp, seagrass, and fern from the world generation."
  }
}
```
### `data\minecraft\worldgen\placed_feature\seagrass_deep.json`:
```json
{
  "feature": "minecraft:seagrass_tall",
  "placement": [
	{
		"type": "minecraft:count",
		"count": 0
    }
  ]
}
```
### `data\minecraft\worldgen\placed_feature\seagrass_normal.json`:
```json
{
  "feature": "minecraft:seagrass_short",
  "placement": [
	{
		"type": "minecraft:count",
		"count": 0
    }
  ]
}
```
### `data\minecraft\worldgen\placed_feature\seagrass_deep_cold.json`:
```json
{
  "feature": "minecraft:seagrass_tall",
  "placement": [
	{
		"type": "minecraft:count",
		"count": 0
    }
  ]
}
```
### `data\minecraft\worldgen\placed_feature\seagrass_deep_warm.json`:
```json
{
  "feature": "minecraft:seagrass_tall",
  "placement": [
	{
		"type": "minecraft:count",
		"count": 0
    }
  ]
}
```
### `data\minecraft\worldgen\placed_feature\seagrass_cold.json`:
```json
{
  "feature": "minecraft:seagrass_short",
  "placement": [
	{
		"type": "minecraft:count",
		"count": 0
    }
  ]
}
```
### `data\minecraft\worldgen\placed_feature\seagrass_river.json`:
```json
{
  "feature": "minecraft:seagrass_slightly_less_short",
  "placement": [
	{
		"type": "minecraft:count",
		"count": 0
    }
  ]
}
```
### `data\minecraft\worldgen\placed_feature\patch_taiga_grass.json`:
```json
{
  "feature": "minecraft:patch_taiga_grass",
  "placement": [
	{
		"type": "minecraft:count",
		"count": 0
	}
  ]
}
```
### `data\minecraft\worldgen\placed_feature\patch_large_fern.json`:
```json
{
  "feature": "minecraft:patch_large_fern",
  "placement": [
    {
		"type": "minecraft:count",
		"count": 0
    }
  ]
}
```
### `data\minecraft\worldgen\placed_feature\patch_tall_grass.json`:
```json
{
  "feature": "minecraft:patch_tall_grass",
  "placement": [
	{
		"type": "minecraft:count",
		"count": 0
    }
  ]
}
```
### `data\minecraft\worldgen\placed_feature\patch_grass_taiga_2.json`:
```json
{
  "feature": "minecraft:patch_taiga_grass",
  "placement": [
	{
		"type": "minecraft:count",
		"count": 0
    }
  ]
}
```
### `data\minecraft\worldgen\placed_feature\patch_tall_grass_2.json`:
```json
{
  "feature": "minecraft:patch_tall_grass",
  "placement": [
	{
		"type": "minecraft:count",
		"count": 0
    }
  ]
}
```
### `data\minecraft\worldgen\placed_feature\patch_grass_badlands.json`:
```json
{
  "feature": "minecraft:patch_grass",
  "placement": [
	{
		"type": "minecraft:count",
		"count": 0
    }
  ]
}
```
### `data\minecraft\worldgen\placed_feature\patch_grass_forest.json`:
```json
{
  "feature": "minecraft:patch_grass",
  "placement": [
	{
		"type": "minecraft:count",
		"count": 0
    }
  ]
}
```
### `data\minecraft\worldgen\placed_feature\patch_grass_jungle.json`:
```json
{
  "feature": "minecraft:patch_grass_jungle",
  "placement": [
	{
		"type": "minecraft:count",
		"count": 0
    }
  ]
}
```
### `data\minecraft\worldgen\placed_feature\patch_grass_normal.json`:
```json
{
  "feature": "minecraft:patch_grass",
  "placement": [
	{
		"type": "minecraft:count",
		"count": 0
    }
  ]
}
```
### `data\minecraft\worldgen\placed_feature\patch_grass_taiga.json`:
```json
{
  "feature": "minecraft:patch_taiga_grass",
  "placement": [
	{
		"type": "minecraft:count",
		"count": 0
    }
  ]
}
```
### `data\minecraft\worldgen\placed_feature\patch_grass_plain.json`:
```json
{
  "feature": "minecraft:patch_grass",
  "placement": [
	{
		"type": "minecraft:count",
		"count": 0
    }
  ]
}
```
### `data\minecraft\worldgen\placed_feature\patch_grass_savanna.json`:
```json
{
  "feature": "minecraft:patch_grass",
  "placement": [
	{
		"type": "minecraft:count",
		"count": 0
    }
  ]
}
```
### `data\minecraft\worldgen\placed_feature\seagrass_simple.json`:
```json
{
  "feature": "minecraft:seagrass_simple",
  "placement": [
	{
		"type": "minecraft:count",
		"count": 0
    }
  ]
}
```
### `data\minecraft\worldgen\placed_feature\seagrass_swamp.json`:
```json
{
  "feature": "minecraft:seagrass_mid",
  "placement": [
	{
		"type": "minecraft:count",
		"count": 0
    }
  ]
}
```
### `data\minecraft\worldgen\placed_feature\seagrass_warm.json`:
```json
{
  "feature": "minecraft:seagrass_short",
  "placement": [
	{
		"type": "minecraft:count",
		"count": 0
    }
  ]
}
```
### `data\minecraft\worldgen\placed_feature\disk_grass.json`:
```json
{
  "feature": "minecraft:disk_grass",
  "placement": [
    {
		"type": "minecraft:count",
		"count": 0
    }
  ]
}
```
### `data\minecraft\worldgen\placed_feature\kelp_cold.json`:
```json
{
  "feature": "minecraft:kelp",
  "placement": [
	{
		"type": "minecraft:count",
		"count": 0
    }
  ]
}
```
### `data\minecraft\worldgen\placed_feature\kelp_warm.json`:
```json
{
  "feature": "minecraft:kelp",
  "placement": [
	{
		"type": "minecraft:count",
		"count": 0
    }
  ]
}
```