# MapExtension


Multimap allows you to load a configuration JSON file (new Leaflet map) that includes different layers of the image of the brain to be analyzed. The MapExtension extension allows you to create new maps, open an existing map, add new layers, download, and configuration options.


![picture](images/menumap.png)

- 1 Map list.
- 2 Layers control.
- 3 Map main window.
- 4 Draw tools.
- 5 Region and markers list.


Within the configuration options it is possible to configure the following:


![picture](images/configuracion.png)

Clicking the + button on the menu at right of the map icon, we can create new maps, load existent maps, and add new layer to the map from file, url, CsvTiles object or guide. Each map can be deleted and exported to Json file.

![picture](images/rightmenu.png)

To create new maps click on "Create map". Map must be named. At the moment the new map is included int the map list, and it is added to the configuration file, and it will be loaded if we open the file in the future.

![picture](images/mapname.png) ![picture](images/map1created.png)

If we have previous configuration file we are able to load it clicking int the "Load map" button. A dialog window will be opened to select the file.

Add new layers to a existen map is very easy clicking "Add layer" button. There are 4 ways to do that:

- File: If we have the file locally.

- Tiles URL: searching on the Internet. Maybe is possible load the layer from remote url. Also, there are many example maps to use.

![picture](images/layerfromurl.png)

- [CsvTiles](https://github.com/gherardovarando/leaflet-csvtiles): From csv file that contains coordinates and other info about the layer.

- Grid: Custom layer. We can set some settings manually.

![picture](images/gridlayer.png)

To export a map to JSON file right click on "Export map" over the desired map to export. A dialog window will be opened to save the map.

 ![picture](images/deleteandexport.png)

 To delete the the selected map, click on "Delete".

Also a map configuration and layer configuration can be loaded with drag and drop. Just drag to the maps region or the configuration region.

![picture](images/dragdrop.png)


Once a map has been loaded it is possible to navigate through all its layers making them visible or invisible as necessary. In the following example we have 4 layers, but it is possible having more depending the kind of maps we are using.


![picture](images/4layers.png)          ![picture](images/mapoptions.png)


MultiMap allows to edit settings of the layers. Right button and click on "Edit". At the moment a control bar appears and we can control the contrast and the transparency of the layer.


![picture](images/edit.png)

Minimum

![picture](images/contrastmin.png)

Maximum

![picture](images/contrastmax.png)

Also is possible to configure the opacity and borders of polygons drawn.

![picture](images/polygonsmin.png)

![picture](images/polygonsconfigured.png)

Clicking on the coloured circle it is possible to set the color of the figure.

![picture](images/setcolour.png)

It is possible to draw diferent kinds of geometric figures and put markers on the image.

![picture](images/regionandmarkers.png)


It is also possible to select or deselect the elements and regions as necessary by clicking on their name in the list.

![picture](images/selecteditems.png)

Clicking in the right buttton is possible to search by name, delete, rename or change the colour of the selected item.

![picture](images/rightbutton.png)

In the side of the layers it is possible too, clicking right button, and appears the same options excepting the color.

![picture](images/rightclicklayers.png)
