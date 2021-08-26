# A basic dropdown menu module for reuse in other projects

## Overview

A dropdown menu with user settable elments and two different outpumodes. Automatically scales it unfolded size to the number of elements.

It can simply be pasted to your project from the ![dropdown_basic.tosc :](dropdown_basic.tosc) template.

![numpad](pics/preview.gif) 

## Interface

### To other controls

The dropdown is a group control and can interface to to other controls trough local messages via its tag property. The tag will be updated when an element is selected after opening the menu, as well as the touch value, to trigger the events in local messages.

### Direct MIDI and OSC messages

Like the local messages, the dropdown can also send MIDI or OSC messages directly. The user just needs to use touch as trigger and tag as the source. Here is a shot from the examples in the template.

![directmidiosc](pics/direct_midi_osc.png)


## Settings

![setelements](pics/settings.png)
 
### Changing the list elements

Just add elements to the list as you like but keep the format of the syntax: {"element1", "element2", ...}

### Changing the outputmode

The outputmode can either be "number" OR "text". Since the concept is, to store the result in the 'tag' of the group and use it further from there, it does not allow for both. But this could be extended by scripting from the groups script.

### Changing the appearance

Changing the color is done by entering the group and changing the color of all elements. Same for the Fontsize and color. Changing the size needs to adjust the variables and constants in the script of the switch button inside the group.

---
There are some workarounds implemented to prevent current issues of Touch OSC, but i can not guarantee 100% functionality or reliability. 
This is a first proof of concept prototype for user modules, with a somehow defined interface, but my aim is to extend or change this to a practical, understandable and reliable almost standard, a userbase can agree on and progress with. 
Using the 'tag' is a very limited workaround, that fits the use case of this numpad, but also is the only practical one to achieve local messages with, so far. Which i think is madatory for the acceptance of basic modules for users with no experience or interest in scripting.
---








