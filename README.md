# Docker_Commands

## Dockerfile

```Dockerfile

FROM openjdk:17
WORKDIR /app
COPY /studentMarks-0.0.1-SNAPSHOT.jar .
EXPOSE 2222:2222
ENTRYPOINT [ "java","-jar","studentMarks-0.0.1-SNAPSHOT.jar" ]

```


## Push

```text
docker build -t image .
docker login
docker tag image_id username/image
docker push username/image

```

## Pull

```text

docker pull username/image
docker run -d -p port:port username/image

```

## Docker install in ubuntu EC2

```shell

sudo su
apt install
sudo apt-get update
apt install docker.io

```
