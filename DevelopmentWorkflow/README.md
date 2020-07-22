# Development Workflow

1. Create a Github repo
2. Repo will serve as central point of coordination for all the code written
3. Two branches -> feature and master
4. Feature will have the code for new features, master will represent a working copy of the code base.

### Travis CI

A continous integration provider. The code on the master is tested using the Travis CI. Travis CI is will inturn push it to web hosting service such as AWS.

### Steps

1. Development
    - Create/change features
    - Make changes on the non-master branch
    - push to github
    - Create Pull Request to merge with master
2. Test
    - Code pushed to Travis CI
    - Run Tests
    - Merge PR with master
3. Production
    - Code pushed to Travis CI
    - Tests run
    - Deploy to AWS 

### How to use Docker here?

    Docker is a tool which makes executing these tasks. 


### Create a sample React project
    ```
    sudo apt install npm
    sudo npm install -g npx
    sudo npx create-react-app frontend
    ```

### Run application

    ```npm run start``` - Start a development server
    ```npm run test``` - Run tests associated with the project
    ```npm run build``` - Builds a production version of the application

#### Docker file for development environment
    Dockerfile.dev is used to in the development environment to start the docker containers

### Docker Volumes

    A reference to the filesystem is created in the container.
    
    Setting up docker volumes
    ``` docker run -p 3000:3000 -v app/node_modules -v $(pwd):/app <image id>```
    the first -v is a placeholder which is not mapped to parent filesystem
    the second -v the present working directory reference is shared with the container

    To avoid this we can use the docker-compose.yml and use it as shorthand for long docker run command

### Run Test 

    Build the image and then run ```npm run test``` overriding the default command.


### Production

    Nginx is a webserver, which takes incoming traffic and respond with some static files(the web page in our case).

    Create another Dockerfile which run the production environment
    - Use node:alpine
    - Copy the package.json
    - Install dependencies
    - Run npm run build
    - Start Nginx - serve the results of the build directory

### Travis CI
    
    - Create a travis.yml file and set up the test suite
    - Tell Travis we need the copy of docker running
    - Build our image using Dockerfile.dev
    - Tell travis how to run our test suite
    - Tell travis how to deploy our code to AWS


