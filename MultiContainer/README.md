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

    If you want to embed images, this is how you do it:

    ![Image of Architecture](/home/gopinath/Desktop/image.jpg)