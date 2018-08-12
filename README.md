# Sample Hello World Dockerfile

javac HelloWorld.java

create manifest.txt

jar cfm HelloWorld.jar manifest.txt HelloWorld.class

Test: java -jar HelloWorld.jar


Create Dockerfile.

Don’t forget to leave the empty line at the end of the file.(Many older tools misbehave if the last line of data in a text file is not terminated with a newline or carriage return / new line combination. They ignore that line as it is terminated with ^Z (eof) instead.)

docker build -t helloworld .

docker images

docker run helloworld

Output: Hello, World

-----------------------------------------------

# Docker login:
docker login
Login with your Docker ID to push and pull images from Docker Hub. If you don't have a Docker ID, head over to https://hub.docker.com to create one.
Username: impks
Password:
Login Succeeded

# Tag images
docker tag helloworld:latest impks/helloworld:latest

# Push to registry
docker push impks/helloworld:latest

# Delete docker container
docker rm e446de44def5

# Delete docker image
docker rmi 4eb4714d8eb8
