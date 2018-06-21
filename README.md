[![Build Status](https://travis-ci.org/claudioaltamura/docker-java8-jetty.svg?branch=master)](https://travis-ci.org/claudioaltamura/docker-java8-jetty)

# docker-java8-jetty
Hello World Web example with docker, Java 8, Jetty and Gradle

## build container
./gradlew createContainer

## start container
./gradlew startContainer

or

docker run --rm --net host <name>

### run example
docker inspect <container id> | grep "IPAddress"

curl -X GET http://<IPAddress>:8080/helloworld

or when container has been started with --net option

curl -X GET http://localhost:8080/helloworld
