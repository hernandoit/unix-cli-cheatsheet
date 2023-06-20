# Unix-CLI cheatsheet

`Table of Contents`

`UNIX`
- [pwd](#pwd), [man](#man), [ls](#ls), [cd](#cd), [mkdir](#mkdir)
- [rmdir](#rmdir), [touch](#touch), [rm](#rm), [mv](#mv), [cp](#cp)

`REPOSITORIES`
- [git](#git)

`BACKEND HOSTING`
- [heroku](#heroku)

`FRAMEWORKS`
- [django](#django)
  
- [honorable mentions](#honorable-mentions)

## `pwd` 
### Description
print working directory; current directory you are in the file system

```md
/Users/<user directory>/Documents
``` 

## `man` 
### Description
manual for for terminal commands; 

```md
man rm 
man ls 
man git
```

## `ls`
### Description
list all files and directories in current working directory

```md
Documents Desktop Downloads
```

`ls -a` - flag to see all, including hidden

```md
.gitconfig .gitignore .vscode
Documents Desktop Downloads
```

`ls -l` - flag for more detailed information

```md
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
drwxr-xr-x  10 <user directory>  staff   320 Jun 30 06:29 sei
```

## `cd`
### Description
change directory

```md
cd Documents 
cd /home/Desktop 
cd Downloads
```

`cd .` - represents the current directory; all part of the <users name> directory

```md
cd ./Documents 
cd ./Desktop 
cd ./Downloads
```

`cd ..` - represents the parent directory; moving up one in the directories

```md
cd .. 
```

`cd ~ ` - home directory of current user; /Users/<users name>

```md
cd ~
```

## `mkdir` 
### Description
make directory

```md
mkdir myDirectory 
mkdir projects 
mkdir users-working-branch
```

## `rmdir `
### Description
remove directory

```md
rmdir myDirectory 
rmdir projects 
rmdir users-working-branch
```

## `touch `
### Description
creates files in a directory

```md
touch index.html style.css contacts.js
```

## `rm` 
### Description
removes files from current directory; use the -r flag to delete folders; use -f flag to force remove something

```md
rm index.html 
rm -r myDirectory 
rm -f users-working-branch 
rm -rf this-working-directory
```

## `mv `
### Description 
move files

```md
mv filename [/new/location/new-filename]
```

## `cp` 
### Description
copy; use the -r flag to copy folders

```md
cp filename [/location/of/new-filename] 
```

## `Git`
`Basic commands`
- `git init` - initializes a repository on terminal
- `git clone` - makes a local copy of a fork: git clone https://url-to-clone
- `git status` - gives status of repository
- `git add` - stages files for committing /// git add index.html
- `git commit` - git commit -m "created a new post.txt file"
- `git reset` - undoes a staged commit
- `git push + [a] + [b]`
- `[a] origin` is a shortcut for the URL of your default remote repository (in this case, the repository on GitHub). You can have many remotes if you want, but we’re only going to work with one for now.
- `[b] master` refers to the branch on your remote repository where you are currently adding your changes. Again, for now, we’re just going to be working on the master branch.
- `git log` - shows a time line of changes and who make the entries

```md
commit 6d33f525a09b9918f75188db164ea2722039830b
Author: Sarah <sarah@gmail.com>
Date: Wed Jan 28 17:44:03 2015 -0500
added a new post
```

`Best practices`
```js
`git branch` - confirm your working on the right branch
`git status` - (to confirm a clean working directory)
`git add [fileName]`
`git status` - (to confirm modified files have been staged)
`git commit -m "If applied, this commit will ..."`
`git log` - (to verify your last commit worked)
```

`commit message template`
A properly formed Git commit subject line should always be able to complete the following sentence:

```md
If applied, this commit will ...

If applied, this commit will refactor subsystem X for readability
If applied, this commit will update getting started documentation
If applied, this commit will remove deprecated methods
If applied, this commit will release version 1.0.0
If applied, this commit will merge pull request #123 from user/branch
```

`Working with other repos`
The workflow for contributing to an open-source product or your dev team’s project comprises the following steps:

```md
1. Forking
2. Cloning
3. Editing
4. Adding/committing
5. Pushing
6. Submitting a pull request
```

## `Heroku`
### Description 
Heroku Command Reference

A full list of Heroku commands can be accessed by running `heroku --help`; below are some of the more common ones.


|   Commands	       |   Behavior 	|   	
|---	               |---	        |
| heroku logs [--tail] |Running just heroku logs will show you the server logs from your deployed                   API. The --tail flag is optional.|   	
| heroku run ...  	   | Run a program from within Heroku. Examples (heroku run rails console, heroku run rails db:migrate). |   	
| heroku config	       | Environmental variables in your current Heroku app. |  
| heroku config:set CLIENT_ORIGIN=https://yourgithubname.github.io| Set CLIENT_ORIGIN |
| heroku apps:rename newname| Rename Heroku app name (entirely optional).|
| heroku restart       | Restart the Heroku app, make sure you do this after changing your API.|
| heroku Open          | Open your Heroku app in default browser.| 	

## `Django`
### Description
Django Command Reference

## pipenv
|  Commands |  Behavior  |
|--- |--- |
|`python -m pip install Django` | installs Django package|
|`pip install Django==<version>` |installs Django package with the specified version ( ex. Django==3.0) |
|`pipenv shell` | starts the Django development environment |
## django-admin
|  Commands |  Behavior  |
|--- |--- |
|`django-admin startproject bigredproject .`| Generate a project folder named `bigredproject` in current directory which is specified by the `.` at the end of the folder name|
|`django-admin startapp api` | Generates an app folder named `api`|


## manage .py
|  Commands |  Behavior  |
|--- |--- |
|`python manage.py shell` | Start up the pipenv shell virtual environment |
|`python manage.py runserver` | Run the Django server |

## migrations
|  Commands |  Behavior  |
|--- |--- |
|`python manage.py showmigrations` | Shows existing migration files |
|`python manage.py makemigrations` | Generate new migration files |
|`python manage.py migrate` | migrates the files |
|`python manage.py migrate <app_name> zero` | "Rollback" or undo ALL migrations |
|`python manage.py migrate 0002` | "Rollback" or undo specific migrations |


## `Honorable Mentions`
### Description
command to change from zsh to bash terminal

```md
chsh -s /bin/bash
```

`paths`

```md
absolute paths : /Users/hernandohernandez/Destop
relative paths : ./../Desktop
```

### Keyboard shortcuts

`Toggle between apps`

```md
command + tab
```

`Spotlight search`

```md
command + space
```

`Tab backwards`

```md
shift + tab
```
