FROM maven:3.6.1-jdk-8-alpine

WORKDIR /app 

COPY . .

RUN mvn package && \ 
    mv target/worker-jar-with-dependecies.jar /run/worker.jar && \
    rm -rf /app/* 


CMD "java" "-jar" "/run/worker.jar" 