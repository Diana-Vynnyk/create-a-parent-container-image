# create-a-parent-container-image
CLOUD: Create a parent container image. Description   It is required to build a parent image, which is a base layer of your image that refers to the contents of the FROM directive in the Dockerfile.

 A sample app from the link: https://github.com/docker/getting-started/tree/master/app

 Create a file named Dockerfile in the same folder as the file package.json with the required contents:   
- image: node:12-alpine
- port: 3000
- workdir: /app
- command: apk add --no-cache python2 g++ make
- copy: . .
- run: yarn install --production
- cmd: ["node", "src/index.js"]

Acceptance criteria 

Docker file is stored in any of SCM              ---- https://github.com/Diana-Vynnyk/create-a-parent-container-image
Image is stored in any container registry        ---- https://hub.docker.com/repository/docker/dvynny/create-a-parent-container-image/general
Container is running
Application is available through a web browser
