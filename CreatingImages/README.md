# Creating a Dockerfile

1. Specify a base image
2. Run some commands to install additional programs
3. Specify a command to run on container startup


-```docker build .``` - run it in the folder containing the Dockerfile

-```docker run <containerID>``` - to run the created image


During the build process, the docker downloads the base image if not available in the cache, run and install the dependencies. The startup command specified is setup when the image is started.

The advantage of Docker is that, it can use the cache if the image is already available making the build process faster.

**Tagging an image**
-```docker build . -t <dockerID>/<project name>:<version>```
Tag the docker image with a name instead of using ID to run the image

Eg : ```docker build . -t gopswamy/redis:latest```



