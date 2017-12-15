### Workspace

The workspace of the application contains the informations present.
Among other things it contains the list of all the maps loaded in the application with the MapExtension, and the setting of the MapExtension.
Moreover whatever extension can save informations in the workspace.


#### Auto-save

MultiMap tries hard :sweat_smile: not lose your work, if you close the application it will reopen (hopefully :pray:) with the same workspace (thus the same maps) even if you did not save the workspace previously.

#### Saving a workspace

We suggest user not to relay too much on the Auto-save ability of MultiMap.
You can save your workspace at any time using the `File > Save Workspace` or `File > Save Workspace As` command.

When a workspace is saved, and thus MultiMap knows where to save it the next time, the path will be showed in the title bar.

Workspaces are saved as simple JSON files.

#### Load a workspace

With `File>Open Workspace` it is possible to select a json file that MultiMap will try to load as a workspace, plese try to open just previously saved workspaces and not others json as that could resolve in a MultiMap failure :fearful:.

#### New workspace

With `File>New Workspace` MultiMap loads a new empty workspace.

#### Solve workspace issues

Sometimes is possible that MultiMap became unusable because of a corrupted workspace, in this case try to close the application and open it again.
If this does not fix the problem you can try to manually delete the auto-save workspace. To do so just delete the file `workspace.json` located in `.multimap > storage` in your home directory (in linux you need to show hidden files to see the `.multimap` directory).
After you manulayy delete the file try to reload the application.
