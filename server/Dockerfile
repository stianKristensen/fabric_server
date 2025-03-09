FROM debian:bookworm

ARG DEBIAN_FRONTEND=noninteractive

RUN apt update -y
RUN apt install -y curl
RUN apt install -y openjdk-21-jre-headless

WORKDIR app

#Install fabric mc server (minecraft 1.21.4, fabric loader 0.16.10, installer 1.0.1) from https://fabricmc.net/use/server/
RUN curl -OJ https://meta.fabricmc.net/v2/versions/loader/1.21.4/0.16.10/1.0.1/server/jar

ENV EULA=true

ENTRYPOINT ["java"]