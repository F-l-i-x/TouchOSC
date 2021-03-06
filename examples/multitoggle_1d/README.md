## Multitoggle examples (exclusive mode)

### ![Multitoggle_Radio_Grid.tosc](Multitoggle_Radio_Grid.tosc)

Dedicated but not restricted to MIDI. All MIDI messages can be set in the scripts individually. Shows the use of arrays, indexing and sending MIDI messages.

![multitoggle](preview_2.gif)

You can see the script interface here:

![script](radio_grid_script.png)



### ![Multitoggle_from_MK1.tosc](Multitoggle_from_MK1.tosc)

A simple multitoggle derived from a copied control from TouchOSC Mk1. Each button can have its own and independent MIDI messages.
Not convenient, not scaleable but usable. Includes scripts to unset the other buttons for 'exclusive mode'.

![multitoggle](preview_1.gif) 

Exclusive mode: When clicked, a button in the group sends its index to its parent (the group)), and the group then
iterates over all of its children (the buttons) and unsets them except for the one which triggered it.