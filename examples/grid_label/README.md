## Labeling a GRID by script

This example shows how to use Lua to iterate over the children of a group (in this case a GRID), and how to index and access their properties, or values.

![gridlabel](preview_1.gif) 


The Button to trigger the labeling notifies the grid with a given name, that the user can set in the script.

![button](script_button.png)


The grid then interates over all of its childs and prepends the name to the index number, thus creating numbered labels.

![gridscript](script_grid.png)

