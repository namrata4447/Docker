FROM alpine
LABEL maintainer "namratamansur@gmail.com"
MAINTAINER 1234
RUN apk add --update nodejs 
RUN apk add npm
RUN apk update
RUN apk add git
RUN git clone https://github.com/aamirpinger/"docker-assignment.git"
RUN mkdir appfolder
RUN ls
WORKDIR /"docker-assignment"
RUN ls
RUN cp -r /"docker-assignment"/node-server-app /appfolder
Q1WORKDIR /appfolder/node-server-app
RUN npm install
ENTRYPOINT node ./src/app.js

