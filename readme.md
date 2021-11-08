# Overview

This application is containerized python flask REST API using Mongo DB (running as a docker container) as the backend database server.

# Installtion and launch

## Launch the MongoDB container

To startup the Mongo DB with sample data, git clone the Github repository at https://github.com/cswclui/mongodb-docker.

`git clone https://github.com/cswclui/mongodb-docker`

## Launch the Flask REST API container

To run and start the API container run the following. It should pull the image from the docker hub and run the container.

`docker run --rm --network ass1 -e MONGO_USERNAME=comp3122 -e MONGO_PASSWORD=12345 -e MONGO_SERVER_HOST='mongo' -e MONGO_SERVER_PORT='27017' -p 9990:15000 polyu18078666d/student_svc`

If you want to explicitly build the image and run the container

- Get to the directory with Dockerfile or pull the image by running `docker pull polyu18078666d/student_svc`
- Run `docker build -t polyu18078666d/student_svc .`
- Run the container using the image

`docker run --rm --network ass1 -e MONGO_USERNAME=comp3122 -e MONGO_PASSWORD=12345 -e MONGO_SERVER_HOST='mongo' -e MONGO_SERVER_PORT='27017' -p 9990:15000 polyu18078666d/student_svc`

# Files

- app.py - Python flask API script with comments
- requirements.txt - contains the names of the python dependencies of the app
- Dockerfile - for building your docker image, with comments)
- readme.md - info about the app
