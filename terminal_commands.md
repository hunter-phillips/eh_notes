# Overview of Terminal Commands
* `man [cmd]` | manual for a command
* `clear` | clear the terminal
* `whoami` | print the current user
* `sudo [cmd]` | run a command as a superuser
* `[cmd] !!` | appends previous command to new command
* `echo [text]` | print to the terminal
* `history` | displays all the commands from the session

## Hotkeys
* `crtl + a` | beginning of a line
* `crtl + e` | end of a line

## Viewing and Changing Directories
* `pwd` | print working directory
* `ls` | list directory contents
  * `ls -la` | list all files and all information
  * `ll` | shortcut for the previous command
* `cd [dir]` | change directory 
  * `.` | link to current directory
  * `..` | link to parent directory
* `cd /` | change to the root directory
* `cd -` | return to previous directory

## Files
* `touch [file]` | create a file
* `cp [file] [new file path]` | copy a file
* `rm [file]` | remove a file
* `nano [file]` | edit a file
  * `^O` | write to disk
  * `^X` | exit nano
* `cat [file]` | print the contents of a file
* `echo [text] >> [file]` | append text to a file
* `echo [text] > [file]` | overwrite a file
* `history > history.txt` | write the session's commands to a file
* `less [file]` | view file contents
* `more [file]` | view file contents

## Directories
* `mkdir [dir]` | make a directory
* `rmdir [dir]` | remove an empty directory
* `rm -r [dir]` | recursively delete a directory and its content

## Users
* `sudo users` | view the users
* `sudo useradd [user]` | add a user
  * `sudo adduser [user]` | alternative
* `sudo userdel [user]` | delete a user
  * `sudo deluser [user]` | alternative

## Package Management
* `sudo apt install [tool]` | install tools

## Networking
* `ping <ip>` | check connection to an address

## Piping
* `[cmd] | [cmd2]` | sends the output of the first command to the second command
  * `history | grep "ping"` | finds occurrences of "ping" 
* `[cmd] | [cmd2] | tee [file]` | prints output of the commands and sends them to a text file
* `cat | grep [search]` | search for a word in a file
