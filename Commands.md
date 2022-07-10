# Commands

<> means argument is optional

[] means argument is required

##  Grim user commands

/grim help - Shows a list of commands and descriptions

/grim alerts - Toggles receiving alert violations

/grim profile [player] - Shows information about a player, such as client version and sensitivity

/grim reload - Reloads all config files, this also resets all online violations

/grim spectate [player] - Go into spectator and teleport to the player

/grim stopspectating - Return to your original position and leave spectator

/grim log [0-255] - Upload a debug log for a prediction flag

/grim verbose - Show every flag, without a buffer

/version GrimAC - check version of GrimAC

## Commands for developers, poking at logic, and debugging

/grim debug <player> - Toggles prediction output

/grim consoledebug <player> - Toggles prediction output into console

/grim sendalert [message] - Internal command to send alert, useful for testing who has permission to see alerts

## Prediction output format

P: Prediction - The best movement that grim thinks was possible as close to actual movement

A: Actual - The actual movement that the client sent to the server

O: Offset - The distance between the predicted and actual movement