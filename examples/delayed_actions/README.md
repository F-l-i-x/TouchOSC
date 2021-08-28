## Example for using timers to achieve delayed actions

Sends an OSC message and then another one 2 seconds later.

![delayed osc](pics/preview.gif)

Makes use of 'update()', 'onValueChanged()', and getMillis().
onValueChanged() sends the fisrt OSC message, takes the current elapsed milliseconds and sets the trigger variable to 'true'.
update() checks for 'trigger' and if its 'true', checks if the elapsed time has exceeded the given delay and in consequence sends the second message and resets trigger to 'false'.

![delayed osc](pics/script.png)
