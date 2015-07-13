[Docker - Build, Ship, and Run Any App, Anywhere](https://www.docker.com/)

## Windows

[Installation on Windows](https://docs.docker.com/installation/windows/)

Read the [glossary](https://docs.docker.com/reference/glossary/) to familiar with the list of terms used around the Docker project.

    whoami@hostname ~
	$ sh /c/Program\ Files/Boot2Docker\ for\ Windows/start.sh
	copying initial boot2docker.iso (run "boot2docker.exe download" to update)
	initializing...
	Latest release for github.com/boot2docker/boot2docker is v1.7.0
	Downloading boot2docker ISO image...
	Success: downloaded https://github.com/boot2docker/boot2docker/releases/download/v1.7.0/boot2docker.iso
	        to C:\Users\whoami\.boot2docker\boot2docker.iso
	Generating public/private rsa key pair.
	Your identification has been saved in C:\Users\whoami\.ssh\id_boot2docker.
	Your public key has been saved in C:\Users\whoami\.ssh\id_boot2docker.pub.
	The key fingerprint is:
	a3:2b:41:4f:f1:f8:18:c2:c3:0f:b5:99:20:f2:cf:81 whoami@hostname
	The key's randomart image is:
	+--[ RSA 2048]----+
	|                 |
	|      .          |
	|       +         |
	|    . + .        |
	|  ...o.=B        |
	|   o.o++.=       |
	|    Do+.+        |
	|    .o++         |
	|     .+o.        |
	+-----------------+
	
	starting...
	Waiting for VM and Docker daemon to start...
	.........................oooooooooooooo
	Started.
	Writing C:\Users\whoami\.boot2docker\certs\boot2docker-vm\ca.pem
	Writing C:\Users\whoami\.boot2docker\certs\boot2docker-vm\cert.pem
	Writing C:\Users\whoami\.boot2docker\certs\boot2docker-vm\key.pem
	
	To connect the Docker client to the Docker daemon, please set:
	    export DOCKER_CERT_PATH='C:\Users\whoami\.boot2docker\certs\boot2docker-vm'
	    export DOCKER_TLS_VERIFY=1
	    export DOCKER_HOST=tcp://192.168.59.103:2376
	
	
	IP address of docker VM:
	192.168.59.103
	
	setting environment variables ...
	Writing C:\Users\whoami\.boot2docker\certs\boot2docker-vm\ca.pem
	Writing C:\Users\whoami\.boot2docker\certs\boot2docker-vm\cert.pem
	Writing C:\Users\whoami\.boot2docker\certs\boot2docker-vm\key.pem
	    export DOCKER_HOST=tcp://192.168.59.103:2376
	    export DOCKER_CERT_PATH='C:\\Users\\whoami\\.boot2docker\\certs\\boot2docker-vm'
	    export DOCKER_TLS_VERIFY=1
	
	You can now use `docker` directly, or `boot2docker ssh` to log into the VM.
	Welcome to Git (version 1.9.5-preview20150319)
	
	
	Run 'git help git' to display the help index.
	Run 'git help <command>' to display help for specific commands.
	
	whoami@hostname ~
	$

Information:

	whoami@hostname ~
	$ docker info
	Containers: 0
	Images: 0
	Storage Driver: aufs
	 Root Dir: /mnt/sda1/var/lib/docker/aufs
	 Backing Filesystem: extfs
	 Dirs: 0
	 Dirperm1 Supported: true
	Execution Driver: native-0.2
	Logging Driver: json-file
	Kernel Version: 4.0.5-boot2docker
	Operating System: Boot2Docker 1.7.0 (TCL 6.3); master : 7960f90 - Thu Jun 18 18:31:45 UTC 2015
	CPUs: 8
	Total Memory: 1.955 GiB
	Name: boot2docker
	ID: ZESD:2WXO:7OSC:W2ZC:2B23:CUDV:35WO:2R2U:VD3M:PVPL:Z4DU:XYZR
	Debug mode (server): true
	File Descriptors: 10
	Goroutines: 17
	System Time: 2015-07-10T13:16:48.628790946Z
	EventsListeners: 0
	Init SHA1:
	Init Path: /usr/local/bin/docker
	Docker Root Dir: /mnt/sda1/var/lib/docker

Version:

    whoami@hostname ~
    $ docker version
    Client version: 1.7.0
    Client API version: 1.19
    Go version (client): go1.4.2
    Git commit (client): 0baf609
    OS/Arch (client): windows/amd64
    Server version: 1.7.0
    Server API version: 1.19
    Go version (server): go1.4.2
    Git commit (server): 0baf609
    OS/Arch (server): linux/amd64

Options:

    whoami@hostname ~
    $ docker
    Usage: docker [OPTIONS] COMMAND [arg...]

    A self-sufficient runtime for linux containers.

    Options:

      -D, --debug=false                                                     Enable debug mode
      -d, --daemon=false                                                    Enable daemon mode
      -H, --host=[]                                                         Daemon socket(s) to connect to
      -h, --help=false                                                      Print usage
      -l, --log-level=info                                                  Set the logging level
      --tls=false                                                           Use TLS; implied by --tlsverify
      --tlscacert=%USERPROFILE%\.boot2docker\certs\boot2docker-vm\ca.pem    Trust certs signed only by this CA
      --tlscert=%USERPROFILE%\.boot2docker\certs\boot2docker-vm\cert.pem    Path to TLS certificate file
      --tlskey=%USERPROFILE%\.boot2docker\certs\boot2docker-vm\key.pem      Path to TLS key file
      --tlsverify=true                                                      Use TLS and verify the remote
      -v, --version=false                                                   Print version information and quit

    Commands:
        attach    Attach to a running container
        build     Build an image from a Dockerfile
        commit    Create a new image from a container's changes
        cp        Copy files/folders from a container's filesystem to the host path
        create    Create a new container
        diff      Inspect changes on a container's filesystem
        events    Get real time events from the server
        exec      Run a command in a running container
        export    Stream the contents of a container as a tar archive
        history   Show the history of an image
        images    List images
        import    Create a new filesystem image from the contents of a tarball
        info      Display system-wide information
        inspect   Return low-level information on a container or image
        kill      Kill a running container
        load      Load an image from a tar archive
        login     Register or log in to a Docker registry server
        logout    Log out from a Docker registry server
        logs      Fetch the logs of a container
        pause     Pause all processes within a container
        port      Lookup the public-facing port that is NAT-ed to PRIVATE_PORT
        ps        List containers
        pull      Pull an image or a repository from a Docker registry server
        push      Push an image or a repository to a Docker registry server
        rename    Rename an existing container
        restart   Restart a running container
        rm        Remove one or more containers
        rmi       Remove one or more images
        run       Run a command in a new container
        save      Save an image to a tar archive
        search    Search for an image on the Docker Hub
        start     Start a stopped container
        stats     Display a stream of a containers' resource usage statistics
        stop      Stop a running container
        tag       Tag an image into a repository
        top       Lookup the running processes of a container
        unpause   Unpause a paused container
        version   Show the Docker version information
        wait      Block until a container stops, then print its exit code

    Run 'docker COMMAND --help' for more information on a command.

Running Docker:

Let’s try the `hello-world` example image. Run `docker run hello-world` command. This should download the very small `hello-world` image and print a `Hello from Docker.` message.

	whoami@hostname ~
	$ docker run hello-world 2>&1 | tee docker_ubuntu_bash.log
	Unable to find image 'hello-world:latest' locally
	latest: Pulling from hello-world
	
	a8219747be10: Pull complete ================================================>]    596 B/596 BB
	91c95931e552: Already exists ===============================================>]     32 B/32 BB
	hello-world:latest: The image you are pulling has been verified. Important: image verification is a tech preview feature and should not be relied on to provide security.
	
	Digest: sha256:aa03e5d0d5553b4c3473e89c8619cf79df368babd18681cf5daeb82aab55838d
	Status: Downloaded newer image for hello-world:latest
	Hello from Docker.
	This message shows that your installation appears to be working correctly.
	
	To generate this message, Docker took the following steps:
	 1. The Docker client contacted the Docker daemon.
	 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
	    (Assuming it was not already locally available.)
	 3. The Docker daemon created a new container from that image which runs the
	    executable that produces the output you are currently reading.
	 4. The Docker daemon streamed that output to the Docker client, which sent it
	    to your terminal.
	
	To try something more ambitious, you can run an Ubuntu container with:
	 $ docker run -it ubuntu bash
	
	For more examples and ideas, visit:
	 http://docs.docker.com/userguide/

Try something more ambitious, you can run an Ubuntu container.

    $ docker run -it ubuntu bash 2>&1 | tee docker_ubuntu_bash.log
    Unable to find image 'ubuntu:latest' locally
    latest: Pulling from ubuntu

    83e4dde6b9cf: Pull complete ================================================>] 65.79 MB/65.79 MBB
    b670fb0c7ecd: Pull complete ================================================>] 71.48 kB/71.48 kBB
    29460ac93442: Pull complete ================================================>]    679 B/679 BB
    d2a0ecffe6fa: Already exists ===============================================>]     32 B/32 BB
    ubuntu:latest: The image you are pulling has been verified. Important: image verification is a tech preview feature and should not be relied on to provide security.

    Digest: sha256:cb90b1a107073ab3e17271e45a6177b23f548b44157d88d955b7e8bcdbcfd14a
    Status: Downloaded newer image for ubuntu:latest
    root@4c6d226fdf33:/#
    root@4c6d226fdf33:/# cat /etc/lsb-release
    DISTRIB_ID=Ubuntu
    DISTRIB_RELEASE=14.04
    DISTRIB_CODENAME=trusty
    DISTRIB_DESCRIPTION="Ubuntu 14.04.2 LTS"
    root@4c6d226fdf33:/#

[Docker Containers on the Desktop](https://blog.jessfraz.com/post/docker-containers-on-the-desktop/)
    
    whoami@hostname ~
    $ docker run -it --name lynx jess/lynx 2>&1 | tee docker_jess_lynx.log


Check the list of (locally) available Docker images.

	whoami@hostname ~
	$ docker images
	REPOSITORY          TAG                 IMAGE ID            CREATED             VIRTUAL SIZE
	jess/lynx           latest              be32844af55b        16 hours ago        134.5 MB
	ubuntu              latest              d2a0ecffe6fa        17 hours ago        188.4 MB
	hello-world         latest              91c95931e552        11 weeks ago        910 B
	
	whoami@hostname ~$

[Docker certs not valid with 1.7](https://github.com/boot2docker/boot2docker/issues/938)

	$ docker ps
	An error occurred trying to connect: Get https://192.168.59.103:2376/v1.19/containers/json: dial tcp 192.168.59.103:2376: ConnectEx tcp: A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond.

Try the below command.

	$ rm -v ~/.boot2docker/certs/boot2docker-vm/*.pem
	$ boot2docker delete && boot2docker init && boot2docker start

## OS X

[Installation on OS X](https://docs.docker.com/installation/mac/)

	$ boot2docker init 2>&1 | tee boot2docker.log
	$ boot2docker start 2>&1 | tee boot2docker_start.log
	$ docker run hello-world 2>&1 | tee docker_hello-world.log

If you see the below message ...

	Post http:///var/run/docker.sock/v1.19/containers/create: dial unix /var/run/docker.sock: no such file or directory. Are you trying to connect to a TLS-enabled daemon without TLS?

Remember that in the previous step ...

	To connect the Docker client to the Docker daemon, please set:
	    export DOCKER_HOST=tcp://192.168.59.103:2376
	    export DOCKER_CERT_PATH=/Users/whoami/.boot2docker/certs/boot2docker-vm
	    export DOCKER_TLS_VERIFY=1

Use the below command to show environment variables for Docker client.

	$ boot2docker shellinit
	
Otherwise, use this shortcut to set to your shell directly.

	$ eval "$(boot2docker shellinit)"

Examples: 

	$  docker run hello-world 2>&1 | tee docker_hello-world.log
	$ docker run -it ubuntu bash 2>&1 | tee docker_ubuntu_bash.log

## Remarks:

Delete all containers. A [container](https://docs.docker.com/reference/glossary/#container) is a runtime instance of a docker image.

	docker rm $(docker ps -a -q)

Delete all images. Docker [images](https://docs.docker.com/reference/glossary/#image) are the basis of containers. 

	docker rmi $(docker images -q)

## Resources

[How to Use Docker on Windows](http://blog.tutum.co/2014/11/05/how-to-use-docker-on-windows/)