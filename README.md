### Unix-CLI cheatsheet

pwd - print working directory; current directory you are in the file system
```
pwd
/Users/<user directory>/Documents
``` 
man - manual for for terminal commands; 
```
man rm 
man ls 
man git
```
ls - list all files and directories in current working directory
```
Documents Desktop Downloads
```
ls -a : flag to see all, including hidden
```
.gitconfig .gitignore .vscode
Documents Desktop Downloads
```
ls -l: flag for more detailed information
```
total 0
drwx------@  7 <user directory>  staff   224 Jun 29 23:52 Desktop
drwx------@ 13 <user directory>  staff   416 Jun 30 01:47 Documents
drwx------+  6 <user directory>  staff   192 Jun 29 11:40 Downloads
drwx------@ 74 <user directory>  staff  2368 Jun 15 21:40 Library
drwx------   5 <user directory>  staff   160 Jun  2 09:05 Movies
drwx------+  5 <user directory>  staff   160 Jun  2 09:05 Music
drwx------+  4 <user directory>  staff   128 Apr  2 17:12 Pictures
drwxr-xr-x+  5 <user directory>  staff   160 May 24 11:07 Public
drwxr-xr-x   4 <user directory>  staff   128 Jun  2 09:05 VirtualBox VMs
drwxr-xr-x  10 user  staff   320 Jun 30 06:29 sei
```

cd - change directory
```
cd Documents 
cd /home/Desktop 
cd Downloads
```
cd . : represents the current directory; all part of the <users name> directory
```
cd ./Documents cd ./Desktop cd ./Downloads
```
cd .. : represents the parent directory; moving up one in the directories
```
cd .. 
```
cd ~ : home directory of current user; /Users/<users name>
```
cd ~
```

mkdir : make directory
```
mkdir myDirectory 
mkdir projects 
mkdir users-working-branch
```
rmdir : remove directory
```
rmdir myDirectory 
rmdir projects 
rmdir users-working-branch
```

touch : creates files in a directory
```
touch index.html style.css contacts.js
```
rm : removes files from current directory; use the -r flag to delete folders; use -f flag to force remove something
rm index.html rm -r myDirectory rm -f users-working-branch

mv : move files
```
mv filename [/new/location/new-filename]
```

cp : copy;use the -r flag to copy folders
```
cp filename [/location/of/new-filename] 
```

## Honorable Mentions

command to change from zsh to bash terminal
```
chsh -s /bin/bash
```

absolute paths : /Users/user/Destop
relative paths : ./Destop


### Keyboard shortcuts

Toggle apps
command + tab

Spotlight search
command + space
