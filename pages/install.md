### Install

You can download the installer for the last version of MultiMap from the [releases page](https://github.com/ComputationalIntelligenceGroup/MultiMap/releases).

The first time the application start it will download and install the basic extensions: MapExtension, ImageJExtension and DevExt, so a working connection is needed.

ImageJExtension need a working Java runtime environment installed in the sistem, [download jre8 here](http://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html).
- **Windows** Download and Install .exe file.
- **Linux** on a terminal `sudo apt install default-jre`

##### The `.multimap` folder

The application configurations, extensions and other files (e.g. the ImageJ installation) are located in a folder named `.multimap` in your home directory (in Linux it will be a hidden folder).

###### How to do a fresh install
If you experience some unresolvable bug at some point you can try a fresh re-install simply by removing the folder `.multimap` and launching the app again, the folder will be created and the basic extensions will be downloaded and installed hopefully resolving the bug.

##### Remove the application

On Windows and Ubuntu you should be able to remove the application from the system using the available applications manager.
You can also remove manually the folder `.multimap` in your home directory.

##### Use the application on macOS

We are not presently able to generate the installer for macOS, to use the application you can directly download the source and start it from terminal:
```
cd multimap
npm install
npm run start
```

You can also build your own installable and so install it in the system.
