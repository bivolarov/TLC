FROM ubuntu:16.04

LABEL Description="Docker image for TLC TP1 application"
EXPOSE 8080

#Update the Ubuntu 
RUN apt-get update 

RUN apt-get install -y \
git \
# General dependencies for MAVEN
openjdk-8-jdk \
maven 

RUN apt-get install -y \
libpng16-16 \
libjasper1 \
libdc1394-22 

# Fetch application code 

RUN git clone https://github.com/barais/TPDockerSampleApp
WORKDIR /TPDockerSampleApp

#Install OPEN CV

RUN mvn install:install-file -Dfile=./lib/opencv-3410.jar \
     -DgroupId=org.opencv  -DartifactId=opencv -Dversion=3.4.10 -Dpackaging=jar
RUN mvn package

CMD java -Djava.library.path=lib/ -jar target/fatjar-0.0.1-SNAPSHOT.jar

