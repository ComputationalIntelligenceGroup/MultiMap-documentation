### My first extension for MultiMap/electrongui

We are going to explain here how to develop an extension form MultiMap (that is an [electrongui extension](https://gherardovarando.github.io/electrongui/API.html#guiextension)).

We will create an extension without any functionality, that can be used as the bareback bone of every extension.

We start from an empty extension and we add different elements, every example presented here can be a working extension, so you can start from every one of this examples to develop your own extension.

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

const {GuiExtension} = require('electrongui')

class MyExtension extends GuiExtension{}
module.exports = MyExtension
```

save `myextension.js` and try to load the extension from MultiMap `Extensions > Install extension > load local extension`. Selecting the `package.json` file in `myextension` folder or directly the `myextension.js` file.

You should see in the `Extensions` menu a new entry `MyExtension`, you can try to activate/deactivate it but nothing will happen because our extension is empty.

##### Add the `activate` method

The activate method of an extension class is where the activation creates the HTML elements, retrieves information from the workspace and create the menus.

So let's add an `activate` method to our class.

```
//myextension.js
const {
  GuiExtension,
  util
} = require('electrongui')

class MyExtension extends GuiExtension {
  constructor(gui) {
    super(gui, {
      menuLabel: 'MyExtMenu',
      menuTemplate: [{
        label: 'toggle',
        click: () => {
          this.toggle()
        }
      }]
    })
  }

  activate() {
    this.appendMenu()
    let pane = util.div('pane padded', 'This is my first extension')
    this.appendChild(pane)
    super.activate()
  }
}
module.exports = MyExtension
```

We pass an object of options to the `super` constructor (see [GuiExtension](https://gherardovarando.github.io/electrongui/API.html#guiextension)) to create a menu entry in the application, the menu is not appended until we call `this.appendMenu()` in the `activate` method.

Moreover in the `activate` method we create an html element (using [`util.div`](https://gherardovarando.github.io/electrongui/API.html#utildivclassname-text)) and we append it to the extension element (GuiExtension extends [ToggleElement](https://gherardovarando.github.io/electrongui/API.html#toggleelement)).

Remember it is important to always call the `super.activate()` method.

You can save the `myextension.js` file and load again the extension from MultiMap.
Now activating the extension will create a new menu from where you can toggle the extension.


##### Buttons

Some examples on how to add buttons.

###### Toggle Button
We will see now how to add a button to toggle the visibility of our extension instead of using the menu as in the previous example.

To do so we use the [`.addToggleButton`](https://gherardovarando.github.io/electrongui/API.html#addtogglebuttonoptions) method of `GuiExtension` class (inherited from `ToggleElement`).
The `id`, `groupId`, and `buttonsContainer` properties of the options passed to the `.addToggleButton` method are compulsory to make the toggle button works properly.
The `icon` property can be whatever [FontAwesome](http://fontawesome.io/icons/) or [PhotonKit](http://photonkit.com/components/) icon class, aletrnatively you can use a `text` property to specify the label of the toggle button.
See electrongui doc for more options of the [`addToggleButton`](https://gherardovarando.github.io/electrongui/API.html#addtogglebuttonoptions) method.


```
//myextension.js
const {
  GuiExtension,
  util
} = require('electrongui')

class MyExtension extends GuiExtension {

  activate() {
    let pane = util.div('pane padded', 'This is my first extension')
    this.appendChild(pane)
    this.addToggleButton({
      id: `${this.constructor.name}_togglebutton`,
      groupId: `${this.constructor.name}_button_group`,
      buttonsContainer: this.gui.header.actionsContainer,
      icon: 'fa fa-space-shuttle'
      //text: 'Toggle it!!!'
    })
    super.activate()
  }

  deactivate(){
    this.removeToggleButton(`${this.constructor.name}_togglebutton`)
  }
}
module.exports = MyExtension
```

###### More Buttons

:memo:
