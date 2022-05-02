FROM node
LABEL maintainer "namratamansur@gmail.com"
MAINTAINER "12345"
RUN apt-get update
#install git
RUN apt-get install git -y
RUN git clone https://github.com/aamirpinger/docker-assignment.git
#create app directory
RUN mkdir appfolder
WORKDIR /"docker-assignment"
#
RUN cp -r /"docker-assignment"/node-client-app /appfolder
WORKDIR /appfolder/node-client-app
#install npm
RUN npm install
ENV CREATEDBY="namrata"
EXPOSE 2000
ENTRYPOINT node ./src/app.js

