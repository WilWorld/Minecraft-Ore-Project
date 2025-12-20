Usage and Terralith integration
--------------------------------

This datapack uses biome tags under `data/ore_scarcity/tags/biomes/` to control which biomes each biome modifier applies to.

To include Terralith biomes (or other mod biomes):

1. Open the tag file that corresponds to the category you want to extend, for example:
   - `data/ore_scarcity/tags/biomes/forest.json`
   - `data/ore_scarcity/tags/biomes/desert.json`
   - `data/ore_scarcity/tags/biomes/ocean.json`
   - `data/ore_scarcity/tags/biomes/cold.json`
   - `data/ore_scarcity/tags/biomes/overworld.json`

2. Add Terralith biome IDs (namespace `terralith:<biome_name>`) to the `values` array. Example:

   {
     "replace": false,
     "values": [
       "#minecraft:is_forest",
       "minecraft:plains",
       "terralith:autumn_forest",
       "terralith:moss_forest"
     ]
   }

3. Reload the datapack or restart the server to apply changes.

Notes:
- Keeping `replace: false` means the pack will include both vanilla biome tags and any mod biomes you add.
- If you prefer to reference mod biome tags directly, add those tags or replace values accordingly.
