# Create a Webapp

- Create a Node JS web App
- Create a Dockerfile
- Build image from Dockerfile
- Run image as container
- Connect webapp from a browser

#### build docker image
```sudo docker build . -t gopswamy/tinywebapp```

#### run docker image
```sudo docker run -p 8080:8080 gopswamy/tinywebapp``` - map the port from host machine to docker container

This will start the container and the web application is listening on port 8080. Open your browser and go to localhost:8080 to access the webapplication.