# jib-test

Steps to test SSH locally:

mvn clean package jib:dockerBuild -DskipTests

docker rm -f test

docker run -d -p 8080:80 -p 22:2222 --name test gkgaurav31/myjava-12032021
#replace the image name with the one specified in pom.xml

ssh root@localhost -p 22
