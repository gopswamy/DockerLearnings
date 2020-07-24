# Multi-container Application

#### Single container Deployment Issue
    - The app was simple - no outside dependencies
    - The image was build multiple times
    - How to connect a DB from a container

### Building a Fibonacci Calculator

    - Backend Architechture inclcudes
        - Nginix server is going to some routing based on user request
        - The frontend request are routed to React server
        - The backend request is routed to Express server which is connected to a Redis and Postgres server

    Architecture:
    

![Image of Architecture](https://github.com/gopswamy/DockerLearnings/blob/master/MultiContainer/image.JPG)
