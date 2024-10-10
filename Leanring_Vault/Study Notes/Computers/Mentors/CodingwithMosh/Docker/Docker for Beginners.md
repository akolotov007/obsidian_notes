programming with Mosh - Docker for beginners
https://www.youtube.com/watch?v=pTFZFxd4hOI

Remainder is from his course
___

# Section 1 
## What is Docker?
- a platform for building, running and shipping applications
- ##### Problems we encounter
	- "it runs on my machine" problem
	- one or more files missing
	- software version mismatch
	- different config settings
- ##### How it solves them
	- by packaging all components into 1 file

## Virtual Machine vs Container
- ##### Virtual Machine
	- an abstraction of a machine (physical hardware)
- **The Problems with VM**
	- each VM needs a full blown OS
	- Slow to start
	- resource intensive
- ##### Container
	- an isolated environment for running application
- **The Benefits of Container**
	- allow running multiple apps in isolation 
	- are lightweight
	- us OS of the host
	- start quickly
	- need less hardware resources

## Docker Architecture
- ![[Pasted image 20241009141437.png]]


![[Pasted image 20241009141630.png]]
- containers are like processes on a computer
- all containers share the kernel of the host
	- a kernel manages the applications and hardware resources

![[Pasted image 20241009141609.png]]


## Development Workflow
- once we create an application, we change it slightly by adding a dockerfile
	- dockerfile = plain text
		- has instructions for docker how to create **docker image** 
- ###### Docker Image includes
	- a cut-down OS
	- a runtime environment (eg Node)
	- Application files
	- third-party libraries
	- environment variables
-  we tell docker to start a **container** using that image

## Docker in Action 
- *follow along*
let's create a simple application in JS that prints "Hello Docker"
make folder
- make file
	- app.js
		- `console.log("Hello Docker!");`

Now, the instructions for dockerizing the app
- Start with an OS
- install Node
- Copy app files
- run `node app.js`

now in the same folder, create a Dockerfile *exactly like this*
```dockerfile
FROM node:alpine
        # all base images can be found on docker hub
COPY . /app
        # copy all files inside the directory into newly created /app
WORKDIR /app
CMD node app.js
```

![[Pasted image 20241009144244.png]]
*the current file layout*
- in terminal : `docker build -t(ag) hello-docker . (dockerfile location)`

we can now check the docker image that was created:
`docker images` or `docker image ls`

and finally we can run it:
`docker run hello-docker`

# Section 2/3
#linux
## Knowing the Linux Basics
- a lot of docker builds upon the basics of linux
- lets get a ubuntu container
	- `docker run ubuntu` // if not found locally, it'll download it and then run it 
- but it doesn't run, it stops prematurely
- we need the -it (interactive) flag
`docker run -it ubuntu`
- now we get a interactive shell

## Managing Packages
- such as:
	- npm
	- yarn
	- pip
	- NuGet
- ubuntu has apt

lets try to install nano
- `apt install nano`
	- unable to locate package nano
	- `apt list` - see the current packages
		- because the local packages are only seen, we need to update the list
- `apt update`
	- now we updated the package list,
*apt install nano*

## Linux File System
![[Pasted image 20241009154231.png]]
- Bin = binaries or programs
- boot = all files related to booting 
- dev = devices
- etc = configuration files
- home = user directories are stored here
- root = home directory of root / only root can access this directory 
- lib = library files / software dependencies 
- var = files that are updated frequently / log files / application data / etc
- proc = files that represent running processes 
- *everything is a file, even devices and processes*

## Navigating the Linux File System
- `pwd`
	- print working directory
- `ls`
	- list files
- `mkdir` - make directory
- `rm -r ` remove recursively 
- `mv` - move / rename
- `touch`  - create
- `rm` - remove file
- ``
[[23. Linux Commands | additional Linux Commands]]

## Editing and Viewing Files
`cat` - concat  / shows all file content
`more` -  shows by pages, can scroll with spacebar
apt install less  / newer version of more 
- `less`
`head -n 5 (filepath)` - shows the beginning files
`tail`  - shows the end of the file


## Redirection 
 - changing the source of input and output (keyboard and screen)
 - `echo thisissometext > text.txt`
 - the '>' is the redirection  

## Searching for Text
`grep` - global regular expression print

`grep (flags) (text) (file_location)`
`grep -i hello file1.txt`
 - `-i ` case insensitive 
 - find hello in file1.txt
`grep -i hello file1.txt file2.txt`
`grep -i root /etc/passwd`
`grep -i -r hello .`
- `-ir` flags can be combined / case insensitive and recursive 

## Finding Files and Directories
`find`
`find -type d` show directories
`find -type f` show files
`find -type f -iname "f*"` show files (case insensitive) starting with "f"

## Chaining Commands
chain without stopping at failing commands`
- `mkdir text ; cd test ; echo done`
AND  
chain commands **and** stopping if command fails
- `mkdir text && cd test && echo done`
OR
`mkdir test || echo "directory already exits"`

PIPING  
output of command into another command
`ls /bin | less `

breaking the chain into multiple lines
`mkdir hello:\`
`cd hello;\`
`echo done`

## Environment Variables
- just like we have vars in programming, 
	- env vars are used to store config for our applications
`printenv PATH`
- `PATH = /usr/local/sbin:/usr/local/bin: ....`

- to temporarily add to the PATH you can export:
	- `export DB_USER=mosh`
	- once you close the terminal, it disappears 

- to permanently add, add to `.bashrc` file   
```bash
cd ~
ls -a 
# .bashrc
#either text edit, or append through redirection
nano .bashrc
echo DB_USER=mosh >> .bashrc
```
 - you have to restart the terminal session for changes to occur
 - `source .bashrc `

## Managing Processes
- `ps`
- PID - process ID
- TTY- which terminal session
- `kill [pid]`

## Managing Users
`adduser - builds on top of useradd`
`useradd -m john`
-  `cat etc/passwd | misleading name, passwords aren't stored here`
``
`usermod` - change user settings
lets change the shell of `john`
- `usermod -s /bin/bash john`

to run docker session as john:
`docker exec -it -u john [container_ID] bash`

`userdel`

## Managing Groups
`groupadd`
`groupmod`
`groupdel`

`groupadd developers`
to check group creation 
`cat etc/group`

users have 1 **primary** group and 0-inf secondary groups
- why?
	- if john creates a file, which group should he use to own the new file that he created
- usermod has 2 flags `-g and -G
	- -g = force group as primary
	- -G = add supplementary groups 

`usemod -G developers john`

check groups of user
`groups john`
- "john | john developers" `every user gets their own group`

## File Permissions
*as root*
- let's create a simple .sh script
- `echo echo hello > deploy.sh`
- to see the permissions:
	- `ls -l`
-rw-r--r--  // `-` is a file, `d` is a directory // 3 groups of permissions shown here

change permissions
`chmod u+x deploy.sh` // add execute permissions to current user (root)
`./deploy.sh` // to run script

to add permissions for others to run:
`chmod o+x john.sh`

# Section 4 

## Images and Containers
- ##### Images
	- contains everything an application needs to run 
	- a cut-down OS
	- a runtime environment (eg Node)
	- Application files
	- third-party libraries
	- environment variables
- ##### Containers
	- provides an **isolated** environment
	- can be stopped and restarted
	- is technically a process

## Sample Web Application
*provided in section4-sample-web-app*
- steps needed:
	- install Node
	- npm install dependencies 
	- npm start

## Dockerfile instructions
- instructions for building image
	- FROM
	- WORKDIR
	- COPY
	- ADD
	- RUN
	- ENV
	- EXPOSE
	- USER
	- CMD
	- ENTRYPOINT
- *notice why we went over linux commands now*


## Choosing the Right Base Image
- docker docs / examples on pre-made base images

```d
FROM node:14.16.0-alpine3.13
```

now do `docker build -t react-app .` to build an image from dockerfile
- `docker run -it react-app` // runs, but shows node.js
	- we want to see the shell, so
	- `docker run -it react-app sh`\

*keep in mind we only created the base image, we have yet to add the application files*

## Copying files and directories
`COPY` - copy files from current directory to in-container directory
- `COPY . /app/` // copy all files to /app 
- `WORKDIR /app`
- `COPY . .` // copy all files to relative path (/app)

`ADD` - 2 additional features
- grab from url like https:/.../.json
- add compressed files | auto decompress them and make it a directory

lesson 35
