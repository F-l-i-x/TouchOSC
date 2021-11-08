## Labeling a GRID by script

### General hint

To ensure that a grid will keep the individual values of its childrens (especially labels), make sure to unlock "current" from "default" values as seen in the follwing picture:

![gridlock](pics/grid_text_lock.png)

### ![Grid_label.tosc :](Grid_label.tosc) 

This example shows how to use LUA to iterate over the children of a group (in this case a GRID, but behaves the same), and how to index and access their properties or values.

![gridlabel](pics/preview_1.gif) 

The button to trigger the labeling notifies the grid with a given name, that the user can set in the script.

![button](pics/script_button.png)

The grid then interates over all of its childs and prepends the name to the index number, thus creating numbered labels.

![gridscript](pics/script_grid.png)


### ![SIMPLE_set_GRID_label_texts-3.tosc :](SIMPLE_set_GRID_label_texts-3.tosc) 

A similar functionality, but done by directly adressing the lables from the buttons and without any iteration.

![gridlabel](pics/preview_2.gif) 

![gridlabel](pics/script_direct.png)  
