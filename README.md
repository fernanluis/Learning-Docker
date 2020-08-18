# Learning-Docker
Learning Docker - https://hub.docker.com/u/fernanluis
Here I have started with the apprenticeship with Docker.

Understanding the main difference between Docker and an Virtual Machine.

Installation using the repository. The key for begin.

OS Ubuntu

~$ sudo apt-get update

~$ sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common

~$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

~$ sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"

Installing docker engine

~$ sudo apt-get update
~$ sudo apt-get install docker-ce docker-ce-cli containerd.io

Like first sample I have execed command hello world:
~$ sudo docker run hello-world

Then, post-installation steps for Linux
Create the docker group.
~$ sudo groupadd docker

Add your user to the docker group.
~$ sudo usermod -aG docker $USER

I continued with somethings commands for install my first image using DockerHub or since terminal.

~$ docker run hello-world

In case of got permission denied while trying to connect to the Docker daemon socket at unix:..
Open the terminal and exec the next command:

~$ sudo chmod 666 /var/run/docker.sock

Until here we have downloaded an image and execed in same time. Two step in one.

The next command provide a images list that we have installed until this moment.
~$ docker image

For download one image (e.g. Ubuntu) exec the next command:

~$ docker pull Ubuntu

Also we can to find an images without login to DockerHub page when we exec the next command:

~$ docker search nameImage

And here we can identifier official images.

Another command that we can exec is echo:

~$ echo "hello world"

echo is a command to show an string for windows or terminal.

~$ docker run -it ubuntu bash 

With the previous command we can to interact with system..

~$ docker ps

Command "docker ps" is a command show the exec the image that we have intalled.

And much more..
