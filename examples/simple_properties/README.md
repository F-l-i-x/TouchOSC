## Two examples for setting properties by local messages and lua script

[properties_localmessage.tosc (no Lua):](properties_localmessage.tosc)

![properties_localmessages](preview_sp.gif) 


[size_color_position_LuaAndLocal.tosc :](size_color_position_LuaAndLocal.tosc)

![setbuttonsizeandposition](preview_sbsap.gif)


Bundled local messages must be set to CONSTANT and its conversion to STRING.

Color bundles must be provided in HEX. (RRGGBBAA)
Frame bundles for local messages must be 4 values (x;y;w;h) separated by semicolons. 
Frame bundles for Lua can be packed by the Rectangle() function. E.g: Rectangle(300,100,50,50)

![properties_localmessages](lm_bundle.png)