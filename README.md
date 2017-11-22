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

- [Nodejs](https://nodejs.org/es/download/) de forma nativa para poder instalar Extensiones.

- La última versión de [Java](http://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html) para ImageJExtension.

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

ImageJExtension is an extension of the original Java tool that allows you to analyze and process images and work in different formats. It also allows to perform different calculations on image pixels, histogram creation, edge detection, filtering and other processing functions. [It is necessary to have the original tool installed](https://imagej.nih.gov/ij/download.html).




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
