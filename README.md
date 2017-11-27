- [Authors](#authors)

- [Overview](#overview)

- [Install](#install)

	- [version](#version)
	- [Requeriments](#requeriments)

- [Main menu](#main-menu)

- [Extensions](#extensions)
	- [Installing extensions](#installing-extensions)


# MultiMap user guide
## v1.0.0


### Authors
 - Gherardo Varando <gherardo.varando@gmail.com>


### Overview

Multimap is a tool designed in the for the viewing and processing of brain images whose function is the extraction of statistical data from them.

### Install



#### version

 - Windows:  [multimap.Setup.exe](https://github.com/ComputationalIntelligenceGroup/MultiMap/releases/download/v1.1.0/multimap.Setup.1.1.0.exe)
 - LINUX (DEB): [multimap.deb](https://github.com/ComputationalIntelligenceGroup/MultiMap/releases/download/v1.1.0/multimap_1.1.0_amd64.deb)




#### Requeriments

- [Nodejs](https://nodejs.org/en/download/) 8.9 or later.

	- Windows: Download and Install .msi file.
 	- [LINUX](https://nodejs.org/en/download/package-manager/): Download from nodesource repository.


- The latest version of [Java](http://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html) for ImageJExtension.

 	- Windows: Download and Install .exe file.
 	- LINUX: ```sudo apt install default-jre```


### Main menu

We have the following headers: 

![picture](images/headers.png)

- 1 File: working with the workspace. **New Workspace**, **Open Workspace**, **Save Workspace**, **Save Workspace as**, **Exit**. 
- 2 Extensions, this tab opens the **Manager** to working with the extensions, allows you to install new extensions (locally or via npm) and activate/deactivate already installed extensions.
- 3 MapExtension: this is the complete [Mapextension](https://github.com/gherardovarando/mapextension). The options are **Show**, **Show Configuration**, **Reload Map**, **Load Map**, **Create Map**, **Export Map**, **Add Layer**, **Settings**.
- 4 Developer tools: it launches an external window that shows the internal elements of the program and a console to execute commands.
- 5 ImageJExtension: executes [ImageJExtension](https://github.com/gherardovarando/imagejextension) The options are **Launch ImajeJ**, **Configure ImageJ**, **Create TileLayer**, **Object Detection**, **Holes Detection**, **Tools**.
- 6 Search bar, to find maps loaded at the moment.

### Extensions

MultiMap is a modular tool which can be expanded through diferent extensions. It uses [electrongui](https://github.com/gherardovarando/electrongui) framework to develop them.


Extensions already present

- [mapextension](http://github.com/gherardovarando/mapextension): creating and viewing Maps. 

- [imagejextension](http://github.com/gherardovarando/imagejextension): processing images and extraction of parameters and objects.

- [GraphicsMagickExtension](https://github.com/gherardovarando/GraphicsMagickExtension): collection of tools and libraries which support reading, writing, and manipulating an image.

- [BioFormatsExtension](https://github.com/gherardovarando/bioformatsextension)



#### Installing extensions

In the latest version of the application, the first time the application is launched, the published extensions will be installed automatically and nothing else will have to be installed.

There are two ways to install extensions:

- Loading the extension locally. For this you have to load the .js file that contains the extension. **Extensions > Install extension > Load local extension**.

- Downloading the npm module if it is published on npm. **Extensions > Install extension > Download npm module**.

![picture](images/searchextension.png)


For more info: [Computational Intelligence Group](http://cig.fi.upm.es/), Universidad Politécnica de Madrid.

