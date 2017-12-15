### My first extension for MultiMap/electrongui

We are going to explain here how to develop an extension form MultiMap (that is an [electrongui extension](https://gherardovarando.github.io/electrongui/API.html#guiextension)).

We will create an extension without any functionality, that can be used as the bareback bone of every extension.

##### Prerequisites

We assume a fairly basic knowledge of javascript, [nodejs](https://nodejs.org/en/) and [electron](https://electronjs.org/). Moreover we will use [npm](https://docs.npmjs.com/).


##### Structure of the npm package

1. First of all create a new folder `myextension`, open a terminal and navigate in it.

2. Create an empty file `myextension.js`.

3. Use now the `npm init` command to initialize a `package.json`, check that the entry point is correctly set to `myextension.js`.

4. Run `npm install electrongui --save` to add `electrongui` to the dependencies of your extension.

##### Writing the MyExtension class

An electrongui extension is just a class that extends `GuiExtension` class.

So lets require the `electrongui` module and export a class.

```
//myextension.js



```
