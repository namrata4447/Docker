FROM ubuntu
MAINTAINER namratamansur@gmail.com
#Install wget,curl,java,maven and tomcat
RUN apt-get update
RUN apt-get install wget -y
RUN apt-get install curl -y
RUN apt-get install openjdk-11-jdk -y
RUN apt-get install maven -y
#install tomcat
RUN wget https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.62/bin/apache-tomcat-9.0.62.tar.gz
RUN tar -xvzf apache-tomcat-9.0.62.tar.gz
RUN mv apache-tomcat-9.0.62 tomcat
RUN rm -rf apache-tomcat-9.0.62.tar.gz

#Install git
RUN apt-get install -y git        
WORKDIR /home/ubuntu/
RUN git clone https://github.com/namrata4447/S3Maven.git

#Set working directory
WORKDIR /home/ubuntu/S3Maven/mavenwebapp/trucks/
RUN ls
RUN pwd
RUN mvn clean install
RUN ls
RUN pwd
WORKDIR /home/ubuntu/S3Maven/mavenwebapp/trucks/target/
RUN ls
RUN pwd
RUN cp -r trucks.war /tomcat/webapps
RUN ls
#Enter environment variable
ENV keys=aatmani

