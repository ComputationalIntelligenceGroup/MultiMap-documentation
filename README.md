# MultiMap user guide
## v1.0.0


### Authors
 - Gherardo Varando <gherardo.varando@gmail.com>


### Overview

Multimap es una herramienta diseñada en el CIG de la UPM para el visionado y procesado de imágenes del cerebro cuya función es la extracción de datos estadísticos de las mismas.

### Install



#### version

 - Windows:  [multimap.Setup.exe](https://github.com/ComputationalIntelligenceGroup/MultiMap/releases/download/v1.1.0/multimap.Setup.1.1.0.exe)
 - LINUX (DEB): [multimap.deb](https://github.com/ComputationalIntelligenceGroup/MultiMap/releases/download/v1.1.0/multimap_1.1.0_amd64.deb)




#### Requeriments

- [Nodejs] (https://nodejs.org/en/download/) natively to install Extensions.

- The latest version of [Java] (http://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html) for ImageJExtension.

- Node Package Manager ([npm](https://www.npmjs.com/)).


### Extensions

Multimap is a modular tool which can be expanded through the development of different extensions that will increase the functionality of the program and allow loading those that are necessary at any time.


Extensions already present

- [mapextension](http://github.com/gherardovarando/mapextension)

- [imagejextension](http://github.com/gherardovarando/imagejextension)



#### Installing extensions


There are two ways to install extensions:

- Loading the extension locally. **Extensions > Install extension > Load local extension**.

- Downloading the npm module if it is published. **Extensions > Install extension > Download npm module**.


#### MapExtension

Multimap allows you to load a configuration JSON file (new Leaflet map) that includes different layers of the image of the brain to be analyzed. The MapExtension extension allows you to create new maps, open an existing map, add new layers, download, and configuration options.


![picture](images/menumap.png)

Within the configuration options it is possible


![picture](images/configuracion.png)

Once a map has been loaded it is possible to navigate through all its layers making them visible or invisible as necessary. By default there are 4 layers:


![picture](images/4layers.png)

- **Centroids**: Centroids of the image.
- **Validation regions**: control regions.
- **guide layer**: regions in which the image is segmented.
- **drawinItems**: in this layer it is possible to create two types of objects, geometric regions (polygons, rectangles, circles) or markers, which serve to delimit the points of a specific region and in order to count the number of centroids that there is within a ragión.


![picture](images/regionandmarkers.png)


It is also possible to select or deselect the elements and regions as necessary by clicking on their name in the list.

#### ImageJExtension

ImageJExtension is an extension of the original Java tool that allows you to analyze, process images and work in different formats. It also allows to perform different calculations on image pixels, histogram creation, edge detection, filtering and other processing tasks. [It is necessary to have the original tool installed](https://imagej.nih.gov/ij/download.html).

#### Install

In order to use this extension it is necessary to configure ImageJ. It is possible to do it in several ways. The latest version of Multimap automatically detects if the extension has been installed and allows you to install all the necessary packages quickly. The following window will appear:

![picture](images/quickinstall.png)

In this way everything will be installed automatically, although it is possible to perform a manual installation selecting the path in **ImageJ > Configure imageJ > Settings** and install it this way: **ImageJ > Configure imageJ > Install ImageJ**. For an optimal behaviour is needed to install all plugins: **ImageJ > Configure imageJ > Download needed plugins**.


ImageJextension adds a submenu to the application menu called "ImageJ". Six main tasks can be done:

![picture](images/imagejmenu.png)

**1. Launch ImageJ**

ImageJ user interface can be launched through "Launch ImageJ" menu entry. This tool can be useful for performing some preprocessing operations to prepare images for Atlas usage.

**2. Configure ImageJ**

ImageJ JVM memory settings (heap and stack) can be configured. By default, Java heap memory is set to 70% of total system memory, and Java stack memory is set to 515MB.

**3. Create Tile layer**

Map Tools is a toolbox for creating Atlas maps. This toolbox is an ImageJ plugin that requires an image or folder with images and the following parameters as input:

    Map name (default: "map").
    Pixel tiles dimension (default: 256).
    Maximum zoom (default: 5).
    Use all slice (default: no): if source image has more than one slice and this option is checked, a map for every slice will be created.
    Merge all slices (default: no): if source image has more than one slice and this option is checked, a max intensity projection (ImageJ ZProjection) of all slices will be performed and the output will be used as input for map creation.
    Slice used (default: 1): if source image has more than one slice, this option allows to choose what slice will be used as input for map creation.
    Output folder: the path where output map will be saved.

With this toolbox, creating layers is also possible. The difference between a map and a layer is that a map contains a JSON configuration file with information about author, map name, and the different layers that make up the map. A map created with this tool will have only one layer. Adding new layers must be done modifying configuration file manually.
**3.1. From image**

When using this option, a dialog will be opened to choose source image, then previously defined parameters can be configured. When this task finishes, the map can be added to the workspace, or the layer can be added to a map in the workspace.
**3.2. From folder**

This option is intended to create a map (or layer) from a big image which is splitted in a small collection of images. Each image name must contain its X and Y coordinates in the big image. For example, partial_image_X0_Y0.tiff will be the image in the left upper corner.

When using this option, a dialog will be opened to choose the left upper corner image, then Atlas needs to combine all images and the user will be asked to configure previously defined parameters and three additional image combination parameters:

    Initial slice (default: 1).
    Last slice (default: 1).
    Scale (default: 1.000): the combined image scale, this parameter goes from 0 to 1 (original size).

When this task finishes, the map can be added to the workspace, or the layer can be added to a map in the workspace.
**4. Object Detection**

Object detection is a tool for detecting objects in an image. For this purpose, obj_detection ImageJ plugin is used, which calculates object centroids using image segmentation techniques. This extension allows to detect objects from a single image, from a folder with many images, or from a list of images, In all cases, following parameters can be configured:

    Minimum radius (default: 1): MaxLoGs Min R parameter.
    Maximum radius (default: 5): MaxLoGs Max R parameter.
    By (default: 1): MaxLoGs step parameter.
    Threshold method (default: "Moments").
    Minimum (default: 1).
    Maximum (default: -1).
    Fraction (default: 0.500).
    Tolerance (default: 0).
    Output folder: the path where detected objects data will be saved, usually the folder with the map of the image being processed is used.

When this task finishes, the layer with detected objects data (called points layer) can be added to a map in the workspace.
**5. Holes Detection**

Holes detection is a tool for detecting holes in an image. For this purpose, obj_detection ImageJ plugin is used, which calculates holes using median filtering and thresholding. This extension allows to detect holes from a single image, from a folder with many images, or from a list of images, In all cases, following parameters can be configured:

    Radius of median filter (default: 10).
    Threshold (default: 250).
    Output folder: the path where detected holes data will be saved, usually the folder with the map of the image being processed is used.

When this task finishes, the layer with detected holes data (called pixels layer) can be added to a map in the workspace.
**6. Mosaic creation**

This tool is located inside "Tools" submenu, it allows to divide a big image into small parts (tiles). The following parameters must be configured:

    Tile size (default: 10): Defines the width and height of the output tiles.
    Original image height (default: 10).
    Original image width (default: 10).
    X0 (default: 0): The start number for generated tiles in X axis.
    Y0 (default: 0): The start number for generated tiles in Y axis.
    Output folder: the path where splitted parts (tiles) will be saved.

Each tile name will be the original image name plus its X and Y position, e.g. original_image_X0_Y0.tif usually will be the upper left corner tile.






### Founding
 This application is been developed by the Computational Intelligence Group (UPM) with the help of the Laboratorio Cajal de Circuitos Corticales (UPM/CSIC) with the economic support of the Spanish Ministerio de Economía y Competitividad through the Cajal Blue Brain Project( Spanish partner of the Blue Brain Project initiative from EPFL) and of the European Union through the Human Brain Project.


### License

The MIT License (MIT)

Copyright (c) 2017 Gherardo Varando (gherardo.varando@gmail.com)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
