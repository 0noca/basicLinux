# Basic

To list directories by time use `ls -alt`
To list dirtectories and put commas in-between them use `ls -dm */` `-d` will return directories, and `-m` will add commas.

# Custom Commands on bash

use the "alias", as in alias `[commandName]="command[1] command[2]"`
e.g
`alias mastertheLS='ls -alt -dm */'` This command will list all the directories with commands, ending  with / and sorts them by date.
