# Docker_Commands

## Dockerfile
FROM openjdk:17
WORKDIR /app
COPY /studentMarks-0.0.1-SNAPSHOT.jar .
EXPOSE 2222:2222
ENTRYPOINT [ "java","-jar","studentMarks-0.0.1-SNAPSHOT.jar" ]


## Push

docker build -t image .
docker login
docker tag image_id username/image
docker push username/image

## Pull
docker pull username/image
docker run -d -p port:port username/image
