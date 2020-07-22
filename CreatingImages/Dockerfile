#Creating a Redis image from Docker file

# Use an existing Docker image as a base
FROM alpine

# Download and install dependency
RUN apk add --update redis


#Tell the image what to do when it starts as a container
CMD ["redis-server"]