# Usage

### Build the container

`-t` tags the application with the name provided.
```docker build -t myapp .```

### Run the container
```docker run -d -p 8080:80 myapp```
`-d` runs the container in detached mode.  
We can start a docker container in detached mode with a `-d` option. So the container starts up and run in background. That means, you start up the container and could use the console after startup for other commands.

The opposite of detached mode is foreground mode. That is the default mode, when `-d` option is not used. In this mode, the console you are using to execute docker run will be attached to standard input, output and error. That means your console is attached to the container's process.

`-p` maps the port from container to the host machine.  
`8080:80` refers `host-machine-port : container-port`. We have exposed the port 80 in container and we can access the webpage in our host machine with `http://localhost:8080`.