programming with Mosh - Docker for beginners
https://www.youtube.com/watch?v=pTFZFxd4hOI

Remainder is from his course
___

# Section 1: What is Docker
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

# Section 2/3 : Linux command line

## Knowing the Linux Basics
- a lot of docker builds upon the basics of Linux
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

# Section 4: Building Images

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
- or set work directory (what we will do)
- in Dockerfile:
	- `WORKDIR /app`
	- `COPY . .` // copy all files to relative path (/app)


`ADD` - 2 additional features
- grab from url like https:/.../.json
- add compressed files | auto decompress them and make it a directory

## Run Command
- `RUN` - runs a command
	- in Dockerfile:  `RUN npm install`
- now lets build the image again
	- `docker build -t react-app .`
	- and run it interactively
	- `docker run -it react-app sh`

## Setting Environment Variables
- `ENV {key=value}`
- in Dockerfile:	`ENV API_URL=http://api.myapp.com`
build image, run a container
- inside container:
	- `printenv` - shows all env vars
	- or
	- `echo $API_URL`

## Exposing Ports
- keep in mind that a container can expose a port that the **host** will not expose.
	-  run `npm start` in project folder `react-app`
		- can connect with `localhost:3000`
	- will happen inside container 
- In Docker-file
	- `EXPOSE 3000` - expose port 3000 / done for documentation over function


## Setting the User
- docker runs containers with root privileges
	- security risk
	- lets go through the step needed to create another user that has less privileges 
-  in alpine:
	- lets create a group and add a system-user to that group
	- `addgroup app` 
- `adduser -S -G app app` // group:app username:app
	- having a user with the same group name is common and best practice in linux   
- `groups app` // show users within the app group

- let's concatenate the commands
	- `addgroup app && adduser -S -G app app`
	- now lets add => Dockerfile

- in Dockerfile
	- `RUN addgroup app && adduser -S -G app app`
	- `USER APP`

## Defining Entrypoints
- try to run the app with `npm start` from image
	- `docker run react-app npm start`
		- get error: permission denied
- what did we forget to do?
	- build the newest image!
	- `docker build -t react-app .`

- in Dockerfile:
	- `CMD npm start`
		- let's add this line so that the container will start npm on launch
	- build new image w/ this change 

But what's the difference btwn `CMD` and `RUN`?
- `RUN` - is when we are building an image
- `CMD`- commands at runtime
	- 2 ways to write out CMD commands ->

- `CMD npm start` - shell form / spawns another shell to run command
- `CMD ["npm","start"]` execution form / runs inside current shell
	- best practice

- `ENTRYPOINT` - similar to CMD | certain that command runs at runtime
	- has shell/exec form 
- `ENTRYPOINT ["npm","start"]`
	- *can easy change the CMD on container start, but with entrypoint, must add --entrypoint flag*
		- `docker run react-app --entrypoint {command}`\

Current dockerfile:
``` D
FROM node:14.16.0-alpine3.13
RUN 
USER app
WORKDIR /app
COPY . .
RUN npm-install
ENV API_URL=http://app.myapi/com/
EXPOSE 3000
# can also be CMD []
ENTRYPOINT ["npm","start"]
```


## Speeding up builds
- our container have layers
	- `docker history react-app`
- we can see the commands and how much space they take up
	- instead of rebuilding an image from scratch
		- compare any changes to a **cache** of the image
- let's modify our dockerfile  
	- separate 3rd party install 

in dockerfile: 
```D
WORKGROUP /app
COPY package*.json .
RUN npm install 
COPY . .
ENV //
```
- build image - regular time
	- now if we change a file (readme.md) 
		- and re-build - way faster build
- **NOTE**
	- anything below a changed command has to be rebuilt from scratch by the docker engine when creating a containers

#### Key Takeaway
- optimize your Dockerfile by having stable instructions at the top, and changing instructions towards the bottom

![[Pasted image 20241010195945.png]]


## Removing Images
- `docker images` 
	- "dangling images"
- `docker image prune` // delete dangling images

- similarly, `docker ps -a` // show all containers
	- `docker container prune` // remove all stopped containers 
- `docker image rm {image_name/ID}` 

## Tagging Images
- 2 ways to tag an image
	- at build
	- post build
- naming conventions:
			- :76, :77
			- :3.1.5 , :3.2
			- :buster, :alice

- **at build**
	- `docker build -t {image}:{tag}`
		- `docker build -t react-app:1.2`
 - **post-build**
	 - `docker image tag {image} {tag}`
		 - `docker image tag react-app:latest react-app:1`
		- `docker image tag b06{ID head} react-app:latest`
- **note** - the latest tag can get out of order
	- since it is only a tag and doesn't automatically apply to the latest build
		- have to manually set it

## Sharing Images
- creating a repo on docker hub
	- then tag image same as repo name
		- ![[Pasted image 20241012111751.png]]
- `docker login`
	-  `docker push codewithmosh/react-app:2`

- make small change in readme (for concept) 
	- then `docker build -t react-app:3 . `  
	- `docker images`
		![[Pasted image 20241012112154.png]]
	- `docker image tag-react-app:3 codewithmosh/react-app:3`
	- `docker push codewithmosh/react-app 3`

## Saving and loading images
- **docker image save**
	- save one or more images to a tar archive 
	- `docker image save -o react-app.tar react-app:3`
- **docker image load**
	- load an image from a tar archive
	- `docker image load -i react-app.tar


# Section 5 : Working with Containers

## Starting Containers
-  `docker ps`
	- see docker running processes 
		- every container is a special process
		- has own file system 
- `docker run -d react-app`
	- -d flag = detached   
- `docker run -d --name blue-sky react-app`
	- giving a name to a container of "blue-sky"


## Viewing the Logs
	`docker log --help`
- *on a running container*
	- `docker logs react-app/{id}`
- see whatever is being written to logs live:
	- `docker logs -f` /feed


## Publishing Ports
`docker run -p {host_port:container_port}`
- `-p 80:3000`

- `docker run -d -p 80:3000 --name c1 react-app`
	- do `ps` to see port mapping


## Executing Commands in Running Containers
- `docker exec {running_container} {command}`
	- `docker exec c1 ls`
- `docker exec -it c1 sh`
	- run an interactive shell in the running container


## Stopping and Starting Containers
- `docker stop/start {container}`
	- `docker stop c1`

## Removing Containers
- `docker rm {container}`
	-  if you try to stop a running container, error:
		- Stop container and then remove
		- or force remove
			- `docker rm -f c1`

- then you can do a `container prune`
	- will remove all stopped containers
		- `docker container prune`

## Containers File System 
- *assuming running container*
	- `docker exec -it {container} sh`
-  if your 2 containers off the same image, they have separate file systems
	- *test it by running 2 containers, adding a file in A and then run an interactive session in B*


## Persisting Data using Volumes
- `docker volume`
	- `create`
	- `inspect`
	- `ls`
	- `prune`
	- `rm`

- `docker volume create app-data`
	- `docker volume inspect app-data`
		- will show mountpoint for the volume:
			- C:/program Files/docker ...
			- /var/lib/docker/volumes/
- now let's use the volume
	- `docker run -d -p 4000:3000 -v app-data:/app/data react-app`


## Copying Files between the Host and Containers
- #### From container to Host
- *in a running container*
	- `docke exec -it {image} sh`
- let's create a simple log file
	- `echo some random characters > log.txt`
	- `exit`
- then we can do copy:
	- `docker cp (from) (to)`
	- `docker cp {image}:{full filepath} {destination}`
		- `docker cp e1c9043ea8ce:/app/log.txt .`

- #### From host to container
	- `docker cp secret.txt e1c:/app`


## Sharing the Source code with a Container
- when publishing changes
	- ##### for production:
		- build a new image every time, and properly tag it 
	- #### for development: 
		- ~~build new image~~
		- ~~copy files~~
		- mapping directory from host to directory to container
		- ![[Pasted image 20241015134118.png]]
- `docker run -d -p 5001:3000 -v $(pwd):/app/data react-app` 
	- run container in detached state
	- host port 5001 -> container port 3000
	- **!** volume maps from current working directory -> containers: /app/data


# Section 6: Running multi-container apps

## Installing Docker Compose
- comes shipped with Docker Desktop by default (for Mac and Windows)
 - `docker-compose --version`

## Cleaning up our our workspace
*this will clear out all your images and containers*
- we know: `docker rm {image} {image2} ... `
	- takes to long
	- `docker image ls -q`
		- lists all images ID

- First remove containers:
	- `docker container rm -f $(docker container -ls -aq)` 
		- forcefully remove all containers including stopped ones
- secondly, remove unnecessary images 
	- `docker image rm -f $(docker image -ls -aq)` 


## The Sample Web Application
- *don't have it, but its a frontend, backend and database*
- has `docker-compose.yml` file
	- *in same directory*
	- `docker-compose up`

## JSON and YAML Formats
- json is a human readable language that holds data about objects:
```json
{
"name" : "The Ultimate Docker Course",
"price" : 149,
"is_published" : true,
"tags" : ["software","devops"],
"author" : {
	"first_name": "Mosh",
	"last_name": "Hamedani",
	}
}
```

same data represented in YAML, 

```yaml
___
name : The Ultimate Docker Course
price : 149
is_published : true
tags :
 - software
 - devops
author:
	first_name: Mosh,
	last_name: Hamedani
```

- why don't we use YAML for everything? 
	- bc parsing is slower in YAML, since all data is read as string and then guessed to be a certain data type


## Creating a Compose File

- to find latest version of compose, check docs
- each service has its own docker file inside of it
``` 
frontend
	|- dockerfile
backend
	|- dockerfile
database
	|- dockerfile
```

```yml
// vidly is the name of the app 
version : "3.8"
services:
	web:
		build: ./frontend
		ports:
			- 3000:3000
		environment: // creating env variables
			DB_URL: mongodb://db/vidly
		
	api:
		build: ./backend
		ports:
			- 3001:3001
	db:
		image: mongo:4.0-xenial
		// pulling an image instead of building one
		ports:
			- 27017:27017
		volumes:
			- vidly:/data/db
volumes:
vidly:

```

## Building Images 
- `docker-compose build`
	- `docker images`
		- vidly_api
		- vidly_web
		- mongo
- if you want a complete re-build wo/ any cache
	- `docker-compose build --no-cache`
	- `docker-compose up`
## Starting and stopping the Application
- combining building and starting
	- `docker-compose up --build`
- running in detached state
	- `docker-compose up -d`
- see running processes
	- `docker-compose ps`
![[Pasted image 20241015145336.png]]

#### To Stop
- `docker-compose down`


## Docker networking
- `docker network ls`
	- 3 default:
		- ![[Pasted image 20241015145543.png]]


- *assuming docker-compose was run, and has running containers*- 
- `docker ps`![[Pasted image 20241015145730.png]]
- let's enter a shell session in the `web` to ping `api`
	- `docker exec -it -u root 8c6 sh`
		- `ping api`

## Viewing Logs
-  `docker logs --help`
	- `docker-compose logs --help`
- `docker logs {image} -f` // follow

## Publishing Changes
- in the project directory:
	- vidly/backend
		- `npm install`
	- reason being is that we will need the dependences installed in order for them to be shared across containers

- in our docker-compose.yml:

``` yaml
// vidly is the name of the app 
version : "3.8"
services:
	web:
		build: ./frontend
		ports:
			- 3000:3000
		environment: // creating env variables
			DB_URL: mongodb://db/vidly
// NEW LINE
		volumes:
			- ./backend:/app
		
	api:
		build: ./backend
		ports:
			- 3001:3001
	db:
		image: mongo:4.0-xenial
		// pulling an image instead of building one
		ports:
			- 27017:27017
		volumes:
			- vidly:/data/db
volumes:
vidly:
```


## Migrating the database
 - *inside project, migrate-database script exists*
	 - goes on to explain how it works, and how to call it

- *in projects docker-compose file:*
```yaml
volumes: 
	- ./backend:/app
// new line
command: migrate-mongo up && npm start
```
- problem: what if our database isn't ready yet when we run this command?
	- solution: wait for it to start

*added wait-for-it.sh script inside backend folder*
```yaml
volumes: 
	- ./backend:/app
// new line
command: ./wait-for db:27017 && migrate-mongo up && npm start

db:
	image:mongo:4.0-xenial
	ports:
		- 27017:27017
```
- long command, lets reduce it to an `entrypoint` script
	- in backend:
		-  `docker-entrypoint.sh`
```sh
#!/bin/bash

echo "waiting for mongoDB to start"
./wait-for db:27017 
 
echo "Migrating the database"
migrate-mongo up 

echo "starting server"
npm start
```
- replace our long command with script:

```yaml
command: ./docker-entrypoint.sh
```


## Running Tests
- *inside frontend folder* 
	- `npm test`
- simple way to test, fast

- can do tests inside a docker as well
- in `docker-compose.yml`
```yaml
services: 
	web: 
		build: ./frontend
		ports:
			- 3000:3000
		volumes:
			 - ./frontend:/app
// lets copy web and make web-tests

	web-test: 
			image:vidly_web 
		volumes:
			 - ./frontend:/app
	    command: npm test 
```

- *in terminal ./vidly*
	- `docker-compose up`
	- in the logs we can see our test being run
	- ![[Pasted image 20241018124017.png]]


# Section 7: Deployment


## Deployment Options
- single host deployment
	- single server
		- if fails, service fails, rip
-  cluster deployment
	- high availability

- cluster solutions
	- built-in: docker swarm
	- google product: Kuberentes

*in the case of this course, Mosh decided to show how to run a single host deployment, and not a cluster, given the complexity of it*


## Getting a VPS (Virtual Private Server)
- VPS Options
	- Digital Ocean
	- Google cloud platform
	- Microsoft azure
	- AWS
	- etc.
- *down the list, from most simple to more complex / being given more options*

*also, your paying for a VPS*


## Installing Docker Machine
![[Pasted image 20241018124637.png]]
- `docker machine` talks to `docker engine` on the server

- does a github pull to install docker machine in ./vidly

## Provisioning a Host
```bash
#! bin/bash
# this can be written in the terminal it's just multiline

docker-machine create \
--driver digitalocean \ 
--digitalocean-access-token b3f0b9d492b7775a5d6.... \ 
# providing an option based on the provider / created in digitalocean
--engine-install-curl "https://releases.rancher.com/install-docker/..."\
# at time of recording, digitalocean had issue, had to pull a prev version of dockerengine
> vidly 
# giving name to server
```


## Connecting to the Host
- `docker-machine ls`![[Pasted image 20241018125739.png]]

- we connect via SSH
	- `docker-machine` abstracts that for us
- `docker-machine ssh vidly`

## Defining the Production Configuration 
- *from docker-compose.yml file*
	- copy content, create new file `docker-compose.prod.yml`
```yml
services:
	 web: 
		 build: ./frontend
	 ports:
		 - 80:3000 # 80 host -> 3000 app
	## deleted volume mapping, and web-test
	restart: unless-stopped
	api: 
		build: ./backend
		ports:
			- 3001:3001
		environment: 
			DB_URL: mongodb://db/vidly
		## deleted volume mapping
		
		restart: unless-stopped
	db:
		image: mongo:4.0-xenial
		ports:
			- 27017:27017
		volumes:
			- vidly:/data/db
		restart: unless-stopped
vidly:
```


## Reducing the Image Size
- *since proj uses react, react has feature to create optimized assets *
	- creates build folder, with all assets optimized

- *from dockerfile, copy and create another*
	- `Dockerfile.prod`
```dockerfile
# step 1: build stage
FROM node:14.16.0-apline3.13 AS build-stage
WORKDIR /app 
COPY package*.json ./
run npm install
COPY . . 
RUN npm run build

# Step 2: Production 
FROM nginx:1.12-apline AS production-stage
RUN addgroup app && adduser -S -G app app
USER app
COPY --from=build-stage /app/build /usr/share/nginx/html
# copying from the build stage (^)
EXPOSE 80
ENTRYPOINT ["nginx", "-g", "daemon off;"]
```

*in ./frontend*:
- `docker build -t vidly_web_opt -f Dockerfile.prod`

- now let's see the change in size 
![[Pasted image 20241018134336.png]]

1 more step, let's configure our `docker-compose.prod` to run `Dockerfile.prod`
*in docker-compose.prod.yml*
```yml
services:
	 web: 
		 build: 
			 context: ./frontend
			 dockerfile: Dockerfile.prod
	 ports:
		 - 80:80 # since we changed the port to 80 for nginx
```

*in terminal ./vidly*
- `docker-compose -f docker-compose.prod.yml build`
- now we optimized both of our images
![[Pasted image 20241018134708.png]]


## Deploying the Application 
![[Pasted image 20241018134821.png]]
- in terminal: `eval $(docker-machine vidly)`
	- now we connected to our machine being hosted on digital ocean

*in connected terminal*
	- `docker-compose -f docker-compose.prod.yml up -d`


## Troubleshooting Deployment Issues

-  `docker-machine ls`
	- given IP of machine, tries to connect, frontend isn't showing

- `docker ps`
	- grab container ID
	- `docker logs {image}`
		- something about perms denied

- *in dockerfile.prod*
```dockerfile
# Step 2: Production 
FROM nginx:1.12-apline AS production-stage

// deleted creation of user | bad from security standpoint, but to prove a point 

COPY --from=build-stage /app/build /usr/share/nginx/html
# copying from the build stage (^)
EXPOSE 80
ENTRYPOINT ["nginx", "-g", "daemon off;"]
```

*in terminal ./vidly*
- `docker-compose -f docker-compose.prod.yml up --build`
	- rebuild images
- now connect to machine IP
	- problem: frontend can't talk to backend
	- troubleshoot with dev tools
		- `api.js` is calling localhost:3001 when it should be calling machine IP:3001

*in api.js*
```js
const baseUrl = process.env.REACT_APP_API_URL || "http//localhost:3001/api"
// REACT_APP_API_URL needs to be set / lets do it in dockerfile
```

*in Dockerfile.prod*
```dockerfile
# step 1: build stage
FROM node:14.16.0-apline3.13 AS build-stage
WORKDIR /app 
COPY package*.json ./
run npm install
COPY . . 
# New line
ENV REACT_APP_API_URL= http://104.131.24.150:3001 

RUN npm run build

```

*in terminal*
- `docker-compose -f docker-compose.prod.yml up --build`

then connect to machine and reload
`docker-machine ls`
- `docker-machine env vidly`
- `eval $(docker-machine vidly)`
- `docker-compose up`

## Publishing Changes
*in production machine terminal*
- `docker ps`
	- we can't see the images version, add that in docker-compose.prod.yml

*docker-compose.prod.yml*
```yml
web:
..
	image: vidly_web:1
api:
	image: vidly_api:1 
```
- lets rebuild `docker-compose -f docker-compose.prod.yml build`

`docker ps`
- can see version of images

manual and time consuming
-  use continuous deployment tools
	- can check latest changes in github and auto tag new images being built 
