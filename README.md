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
```
'r' (read) = 4

'w' (write) = 2

'x' (execute) = 1

no permissions = 0
```
To set read, write and execute permissions to file owner, sum up all values '4+2+1 = 7'.

To set read and write permissions to file group, sum up read and write values '4+2 = 6'.

To set only read permissions to everybody else use value '4'.

touch new_file.txt

chmod 600 new_file.txt

# Changing ownership (chown)

chown username filename.txt

chown username:groupname filename

chown -R username:groupname dirname

# Searching for files and folders (find)

To search for exact file name 'client.conf' in /etc folder, type in following command: `find /etc -name 'client.conf'`

If you want to search for all files with extension '.conf, type in following command in you terminal: `find /etc -name '*.conf'`

`'file*'` - will search for all files and folders which begin with `'file'`

`'*file'` - will search for all files and folders which end with `'file'`

`'*file*'` - will search for all files and folder which has `'file'` in any place

# Searching for text in files (grep command)

`grep 'Directory' /etc/rsyslog.conf`

If you want to search case-insensitively, you have to use '-i' option: `grep -i 'Directory' /etc/*.conf`

# Downloading files from the internet (wget)

`wget https://filesamples.com/samples/document/txt/sample1.txt`

`cat sample1.txt`
#

If you want to save file with different name, use '-O' 

`wget https://filesamples.com/samples/document/txt/sample1.txt -O new_name.txt`

# Command line history (history)

`history`

For a specific search use:
`history | grep mkdir`

# Encoding with Base64

`echo -n 'Text that will be base64 encoded' | base64`

Use pipe to use another program again/ new one.

`echo -n 'Text that will be base64 encoded' | base64 | base64`

`echo -n 'VGV4dCB0aGF0IHdpbGwgYmUgYmFzZTY0IGVuY29kZWQ=' | base64 --decode`

`echo -n 'VkdWNGRDQjBhR0YwSUhkcGJHd2dZbVVnWW1GelpUWTBJR1Z1WTI5a1pXUT0K' | base64 -d | base64 -d`

## Steganography

steghide --help

apt-get -y install steghide

echo 'Secret message.' > secret.txt

cat secret.txt

wget https://raw.githubusercontent.com/ianare/exif-samples/master/jpg/gps/DSCN0042.jpg

steghide embed -ef secret.txt -cf DSCN0042.jpg

steghide extract -sf DSCN0042.jpg -xf secret_extract.txt

