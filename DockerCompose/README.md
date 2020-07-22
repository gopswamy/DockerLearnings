# Docker Compose

Build a Docker container with a simple application involving two components.
The application is will count the number of instance the webpage is visited. 
The database and application is ditributed between two different docker containers.

1. One Docker container contains the Node app
2. The second container has the redis server to store.

The two containers are two standalone processes. There has to be somekind of networking between the two containers for the communication.
Docker compose is a seperate tool which is installed along with Docker. It is used to start up multiple Docker containers at the sametime. Automates the commands which are passed through 'docker run'.

The docker-compose.yml file is used to write up commands to be used in docker run.

```docker-compose up``` - docker run image

```docker-compose up --build``` - to build/rebuild and run the image

```docker-compose down``` - to stop all the containers