### Extensions

MultiMap is a modular tool which can be expanded through different extensions.
MultiMap is built on top of [electrongui](https://github.com/gherardovarando/electrongui) so every electrongui extension will work.

When the application starts for the first time it will install automatically the following extensions:

- [mapextension](http://github.com/gherardovarando/mapextension): creating and viewing Maps.

- [imagejextension](http://github.com/gherardovarando/imagejextension): processing images and extraction of parameters and objects.



#### Installing extensions

![picture](images/installextensions.png)


  There are two ways to install extensions:

  - Loading the extension locally. For this you have to load the .js file (or the associated package.json) that contains the extension. **Extensions > Install extension > Load local extension**.

  - Downloading the npm module if it is published on npm. **Extensions > Install extension > Download npm module**. The user can search the npm registry and select the extenison to install.

  ![picture](images/searchextension.png)
