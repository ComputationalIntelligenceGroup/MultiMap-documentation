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

Multimap es una herramienta modular la cual puede ir ampliándose mediante el desarrollo de diferentes extensiones que apliarán la funcionalidad del programa y permitirá cargar las que sean necesarias en cada momento.


Extensions already present

- [mapextension](http://github.com/gherardovarando/mapextension)

- [imagejextension](http://github.com/gherardovarando/imagejextension)



#### Installing extensions


Existen dos formas de instalar extensiones:

- Cargando la extensión de forma local. **Extensions > Install extension > Load local extension**.

- Descargando el módulo de npm si está publicado. **Extensions > Install extension > Download npm module**.


#### MapExtension

Multimap permite cargar un archivo JSON de configuración (nuevo mapa de Leaflet) que incluye diferntes capas de la imagen del cerebro que se va a analizar. La extensión MapExtension permite crear nuevos mapas, abrir un mapa existente, añadir capas nuevas, descargar, y opciones de configuración.

%%%%%%%%%%%%%%%%%%%%%%%%menu.png


Dentro de las opciones de configuración es posible

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%configuracion.png
![picture](Imágenes/configuracion.png)

Una vez se ha cargado un mapa es posible navegar por todas sus capas haciendo estas visibles o invisibles según sea necesario. Por defecto existen 4 capas: 

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%4layers.png

- Centroids: Centroides de la imagen.
- Validation regions: regiones de control.
- guide layer:  regiones en los que la imagen está segmentada.
- drawinItems: en esta capa es posible crear dos tipos de objetos, regiones geométricas (polígonos, rectángulos, círculos) o marcadores, que sirven para acotar los puntos de una región específica y de cara a contar el número de centroides que hay dentro de una ragión.

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%regionandmarkers.png


También es posible seleccionar o deseleccionar los elementos y regiones según sea necesario haciendo click sobre su nombre en la lista.

#### ImageJExtension

ImageJExtension es una extensión de la herramienta original en Java que permite analizar y procesar imágenes pudiendo trabajar en distintos formatos. Permite además realizar diferentes cálculos sobre los pixeles de la imagen, creación de histogramas, detección de bordes, filtrado y otras funciones de procesamiento. [Es necesario tener instalada la herramienta original](https://imagej.nih.gov/ij/download.html).




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
