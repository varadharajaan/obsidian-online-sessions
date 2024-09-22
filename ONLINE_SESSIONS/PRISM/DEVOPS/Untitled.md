---
created: 2024-09-21T18:36
updated: 2024-09-22T20:15
---


how to build different programming applications
-  java - jar
- python - .zip .pkg
- dotnet
- node

Containerization and Orchestration
-  Docker - continersation tool - conterinerd, packer, runc
- docker compose
- Kubernetes or K8s - orchestration tool

Docker containers
- **Linux container**
- Windows container

Installation of Docker:
- Docker Desktop (windows)
- Docker Engine

Docker commands:
docker build  
docker pull image_name
docker run image_name
docker push image_name

git pull
git push -> remote_url


docker image - bundled version of your app and depdencies
docker container - running version of image in mini linux VM

how to execute the existing docker image from docker repo
how to build custom docker image and publish to repo and pull & run in VM\


h2 DB - in memory DB

username/image-name:tag

node app docker file

1. extend the base image - node or python or java
2. set the workdir
3. copy server.js package.json package.lock.json to docker
4. copy . .
5. run node server.js
mvn clean install 
npm install 

cmd - the value be overridden by the command line arguments

docker run varad/todoapp  app.js



