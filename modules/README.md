# A collection of reusable modules

## Overview

The containing modules are an early approach to achieve reusability of grouped tosc control for different application. They use less to heavy scripting and can be copied directly into your own project.

## Dropdown menu scrollable

![numpad](dropdown_scroll/pics/preview


## Dropdown menu static

![numpad](dropdown_scroll/pics/pre


### Direct MIDI and OSC messages

Like the local messages, the dropdown can also send MIDI or OSC messages directly. The user just needs to use touch as trigger and tag as the source. Here is a shot from the examples in the template.

![directmidiosc](pics/direct_midi_osc.png)


## Settings

![setelements](pics/settings.png)
 
### Changing the list elements

Just add elements to the list as you like but keep the format of the syntax: {"element1", "element2", ...}

### Changing the outputmode

The outputmode can either be "number" OR "text". Since the concept is to store the result in the 'tag' of the group and use it further from there, it does not allow for both. But this could be extended by scripting from the groups script.

### Changing the size when dropped down

The number of elements to show when dropped down (unfolded) can be set by the 'unfoldsize' variable.

### Changing the appearance

Changing the color is done by entering the group and changing the color of all elements. Same for the Fontsize and color. Changing the size needs to adjust the variables and constants in the script of the switch button inside the group.

---
There are some workarounds implemented to prevent current issues of Touch OSC, but i can not guarantee 100% functionality or reliability. 
This is a first proof of concept prototype for user modules, with a somehow defined interface, but my aim is to extend or change this to a practical, understandable and reliable almost standard, a userbase can agree on and progress with. 
Using the 'tag' is a very limited workaround, that fits the use case of this numpad, but also is the only practical one to achieve local messages with, so far. Which i think is madatory for the acceptance of basic modules for users with no experience or interest in scripting.
---








