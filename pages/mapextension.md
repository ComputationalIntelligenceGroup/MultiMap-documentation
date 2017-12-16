### MapExtension


The MapExtension is the fundamental extension of MultiMap, it permits to load a configuration file (in [map.json](https://github.com/gherardovarando/map.schema.json) format), create, export and mainly visualize maps.

#### What is a map

A map is just an ensemble of layers, every layers can be one of the following:
- TileLayer, tiled images.
- deepZoom images (not yet but soon)
- imageLayer, one image rendered in given bounds (just small images can be renderd this way)
- csvTiles, points loaded from tiled csv.
- featureGroup/layerGroup layer (usually markers or shapes) grouped.
- polygon, rectangle, circles
- markers


#### Load a map

To load a map you can either select the map.json file from the menu `Maps > Load map` or dragging the map.json file into the application, in the maps list.

If in the map is defined a `basePath` variable MultiMap will show a warning and ask you if you want to redefine locally the `basePath` value (just do it for locally saved maps).



#### Create a map

To create a new map

#### Add layers

#### Export the map
