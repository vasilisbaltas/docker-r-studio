# Docker-r-studio
 R studio in a container

## Description

To allow usage of R-studio in a portable way using Docker Container

## Procedure


### Build the Container
'docker login'                                                           to authenticate
'docker build -t <Docker Hub username>/<image name> . '                  to build image


### Run the Container 
docker run --rm -p 8787:8787 -e USER=myself -e PASSWORD=guest -v "C:\Courses\Docker w. R\Rstudio shared":/home/myself/r-studio vbaltas/docker-r-studio

where --rm means remove container after running
      -e is used to set username and password
      -v is used to map computer files to the container file system


### Push to docker Hub
docker push vbaltas/docker-r-studio