# docker
go to spring.io select maven 21/17 version add springweb dep
open it intelligi
add package controller 
testcontroller getmapping return hellodocker
try running in local

generate jar
go to file project structure -> artifact click on + symbol new selct class and ok
jar will be generated in out folder
next go to build build artifact -> build
open out

add this in docker image
FROM openjdk:21
COPY out/artifacts/demo_jar/demo.jar demotest.jar
ENTRYPOINT ["java", "-jar", "/demotest.jar"]

docker commands
docker build -t demo1 .
docker images
docker rmi -f image id
docker run -p 8080:8080 demo1

or try running from docker


