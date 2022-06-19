# Punishments

    Punishments:
      Simulation:
        remove-violations-after: 300
        checks:
          - "Simulation"
          - "GroundSpoof"
          - "Timer"
          - "NoFall"
        commands:
          - "100:40 [alert]"
          - "100:100 [webhook]"
          - "200:0 kick %player% incorrect movement!"

Simulation is the name of the check group, it is ignored by grim, and is meant to be a helpful description for the check group

remove-checks-after gives the amount of seconds that it will take from grim to remove a user's flags from this group.  By default, flags will expire after 5 minutes.  You may lower thresholds and this amount to make grim alert faster, or increase threshold and amounts to let grim work with more data and therefore reduce falses.

checks matches checks with the name containing this text and puts them into this command group.  Checks may belong to multiple groups.

Commands will run when the threshold is met.
- The first number is the threshold, the command will only execute when the number of non-expired violations match or exceed this number
- The second number is the interval. The command will only flag once for every 40 times the user flags, for example.  Flags expiring will make it alert at 134 violations for example.  When the command is below the threshold, it will not change affect the next interval flag.
- All subsequent text is the command itself


## Commands

- [alert] is a special command that will send a in-game alert
- [webhook] is a special command that will send a discord webhook
- You may put any other text here as the command, do not include the brackets

## Placeholders

- %check_name% - Name of the check flagging, such as BadPacketsA
- %vl% - Total number of violations
- %verbose% - Extra information about the flag, if available
- %player% - The name of the player
