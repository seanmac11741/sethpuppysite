#website for selling puppies#

docker commands: 
#to (re)build image from a Dockerfile run this 
docker build -t seanmac/node-web-app .

#to deploy container based on above image, run 
docker run -it -p 9000:8080 -v $(pwd):/app seanmac/node-web-app
#in background
docker run -it -d -p 9000:8080 -v $(pwd):/app seanmac/node-web-app


#to display all images run this
docker images

#to run the image and display stuff to web browser run this. -p redirects public port to private port inside docker container 
docker run -it -p 9000:8080 seanmac/node-web-app
#to get docker containers ID run 
docker ps 
#to get logs, run
docker logs <container id>
#to enter the container run 
docker exec -it <container id> /bin/bash
