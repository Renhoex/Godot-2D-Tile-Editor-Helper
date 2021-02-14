# Godot 2D Tile Editor Helper
Godot's tileMap editor interface is decent but incredibly slow to use, this script is designed to give an easy to use and fast interface to speed up the tile laying process

## Script
This does have a godot template but if you just want the code just get the `TileEditorPlus.gd` file.

## Set up
In a 2D scene, make sure you have a tilemap set up with a tileset, create a 2D node child to the tilemap and apply the script to the new child.

## Controls
The script works as a point and click interface, to activate the tool click the "Active" Box.<br />
If you want to move the menu you can move the node and the menu will follow. <br /><br />
**Right click** to swap between copy and paste modes, a message in the output menu will tell you what mode you're in, your cursor will be white when you're in paste mode, and blue when you're in copy mode.<br /><br />
Use the **Left mouse** button to use the copy and paste modes.<br /><br />
**Flip X and Y** will flip your selection on it's corresponding X and Y axis and mirror the image.<br /><br />
**Tiles** will bring up a menu showing all your tiles available so you can quickly copy your tiles out<br /><br />
**Stamp** will show a tileset template, similar to tiles but in a customizable pattern<br /><br />

## Stamps
To select a stamp set, select the node and from the "Set" dropdown menu, select the stamp set you want to use.
To create a new stamp set
- Create a layout for the stamp set using your current tileset
- deactivate the editor (it's important to click the active button), select the node, then check the "Copy Layout" checkbox, this will copy your current tilemap to an array on your clipboard
- open the editor sctipt and find the "STAMP" const, create a new line in the array and paste your tilemap, for the sake of convenience I kept this as one array but you may want to create a global variable in another script file if you plan on modifying this script and don't want it to lag
- on the above variable "Set" add a name to the tool tips so that you can set your tool to use the new stamp
- go back to the 2D scene, click Active and then click Stamp, if you followed the steps correctly you should get a stamp layout of the tilemap layout you set up.


# Important notes and issues
- When you're not using the editor, make sure you deactivate it, the editor will still place tiles even when you interact with godots interface, even if you switch to the code tab.
- Undo and re-doing I couldn't set up so make sure you're careful making your layouts (it's a good idea to create a collection of stamps), my suggestion is to save often and re open the scene if you make a mistake that's too big
