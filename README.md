# Basic

To list directories by time use `ls -alt`
To list dirtectories and put commas in-between them use `ls -dm */` `-d` will return directories, and `-m` will add commas.

# Custom Commands on bash

use the "alias", as in alias `[commandName]="command[1] command[2]"`
e.g
`alias mastertheLS='ls -alt -dm */'` This command will list all the directories with commands, ending  with / and sorts them by date.

`pwd` To see your current dir

# Moving through dirs

`cd /var/log` to move to given folder

`cd ..` To move one directory up
`cd -` to move to previous dir
`cd` home folder

# Listing dir contents

`ls` Lists everything in current dir

`ls /etc/` to list contents of given folder

`ls -la` lists with detailed information

'd' - specifies the folder

'-' - specifies regular file

'l' - specifies symbolic link

# Displaying file content
`cat`

`cat /etc/passwd` (file name)

# Reading file content with strings

`strings /usr/bin/ls` it shows only readable characters from binary files

# Creating files (touch)

`touch file.txt`

# Creating directories (mkdir)

`mkdir [directoryName]`

# Removing files (rm)

`rm file_01.txt`

`rm -d folder_name` to remove empty directories

# Copying files and dirs (cp)

`cp file.txt file_backup.txt`

To copy to another directory do `cp file.txt /tmp`

To copy full directory do `cp -R Pictures /opt/backup`

# Moving and renaming files and dirs (mv)

`mv file.txt /tmp`

`mv file.txt file1.txt` for renaming/ rename do this

`mv file.txt file1.txt /tmp` to move multiple files do this

```
The file owner (user) - 'u'

The group members (group) - 'g'

Everybody else (others) - 'o'
```
```
Three permission types apply to each class:

    The read permission - 'r'

    The write permission - 'w'

    The execute permission - 'x'
```
    
# Changing permission (chmod)
