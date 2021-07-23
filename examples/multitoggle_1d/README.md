## Multitoggle examples (exclusive mode)

### ![Multitoggle_Radio_Grid.tosc](Multitoggle_Radio_Grid.tosc)

Dedicated but not restricted to MIDI. All MIDI messages can be set in the scripts individually.

![multitoggle](preview_2.gif)




### ![Multitoggle_from_MK1.tosc](Multitoggle_from_MK1.tosc)

![multitoggle](preview_1.gif) 

A simple multitoggle derived from a copied control from TouchOSC Mk1. Each button can have its own and independent MIDI messages.
Not convenient, not scaleable but usable. Includes scripts to unset the other buttons for 'exclusive mode'.

Acts as in exclusive mode: When clicked, a button in the group sends its index to its parent (the group)), and the group then
iterates over all of its children (the buttons) and unsets them except for the one which triggered it.