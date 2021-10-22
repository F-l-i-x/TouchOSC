## Increment - decrement for MIDI messages

### ![pgm_incdec.tosc :](pgm_incdec.tosc)

Makes use of the 'tag' property of a button, to store a number beeing used in MIDI or other messages. 
Uses local messages between the buttons and the label to update the current variable, and a little script for the in- and decrement of the number in the tags.

![properties_localmessages](pics/preview.gif) 

Here you can see how 'tag' is used as a value in MIDI messages.

![tag_in_PGM.png](pics/tag_in_PGM.png)

Here is another example using the tag as a CC value:

![tag_in_CC_value.png](pics/tag_in_CC_value.png)

### ![pgm_incdec_lua_only.tosc :](pgm_incdec_lua_only.tosc)

The same funtionality, but without any local messages and without the 'tag' workaround. Therefore MIDI messages must be sent from script aswell. 
The first button stores the number as a local variable and does all the job of in/dec and sending the midi messages. The second button just notifys the first to do something. 

![lua_only.png](pics/lua_only.png)