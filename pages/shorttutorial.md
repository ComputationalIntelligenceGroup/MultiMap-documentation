#### The super short tutorial :rocket:

The fastest way to learn how to use MultiMap via examples.


- ##### Set ... ready ...
 So let's assume you downloaded the MultiMap installable and you run it, then let's open the application for the first time.

 On the first run the application will start downloading three extensions, allow the process to finish.

- ##### Activate extensions

  Once the extensions are installed we have to activate them.

  1. First of all activate MapExtension by selecting `Extensions > MapExtension` a :ballot_box_with_check: should appear next to it.

  2. Then activate ImageJ extensions, and select `Auto Quick-install` in the dialog. The wait the process to finish, ImageJ extension is installing ImageJ and the needed plugins.

  :warning: **You need a working internet connection** :warning:

- ##### Create your first map

  1. Click on the map button in the top left of the application, this will toggle the MapExtension and show the main map pane.

  2. Select the :heavy_plus_sign: button next to the map toggle button and then the `Create map` option.

  3. Chose a fancy name for your first map.

  You have done it! :smile: Your first map should appers in the maps' list on the left of the pane.

- ##### Let's make a layer

  TileLayers are the core of every map, they represent the graphical informations. To create a TileLayer we will use the ImageJ extension.
  First of all let's check that ImageJ can work properly with the application.

  1. If you didn't already activate ImageJExtension do it now.
  2. From the ImageJ menu select `Launch ImageJ`.
  3. If ImageJ opens (can take 1/2 sec) you are ready to go, otherwise reed ImageJExtension [doc](ImageJExtension.md).

  Now we need an image to work with, you can use whatever image for this step but let's use [this image](https://www.goodfreephotos.com/united-states/wisconsin/wildcat-mountain-state-park/wisconsin-wildcat-mountain-state-park-the-starry-skies.jpg.php).

  1. Make a folder in your computer somewhere and call it `Test_Map` (you can use whatever name without spaces, btw spaces in filenames are evil)
  2. Copy the [image](https://www.goodfreephotos.com/united-states/wisconsin/wildcat-mountain-state-park/wisconsin-wildcat-mountain-state-park-the-starry-skies.jpg.php) in the folder (the image could be placed wherever, but let's try to be organized :ok_woman:)

  Now, (finally!!) we can create our layer.

  1. Select the menu entry `ImageJ > Create TileLayer > from Image` and select the image you downloaded in the `Test_Map` folder (or wherever you placed it, we told you to be organized...:expressionless:).
  2. Give a name to your layer, for example `star_layer`.
  3. Select the output folder `Test_Map` using the lower-left button.
  4. Create.

  MultiMap will silently lunch an Imagej process and start building the layer. You can see the progress in the Tasks Manager (the upper-right button).
  Let's now wait until the task finish.

- ##### Add the layer to the map

  We can now add the layer to the map we previously created.

  1. Select the map (a blue mark is shown on the left of the name if the map is selected)
  2. Press the :heavy_plus_sign: and select `Add layer > File`.
  3. Navigate to `Test_Map` folder, a folder named `star_layer`, inside you can find a file named `star_layer.json` open it.
  4. Confirm that you want to add the layer.

  Now you should see the layer appearing in the map.
