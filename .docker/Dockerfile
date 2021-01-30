# See: https://github.com/evolvedpacks/base-image/blob/master/Dockerfile
FROM evolvedpacks/base:latest

ARG VERSION=latest

ENV XMS=1G
ENV XMX=3G

WORKDIR /var/server

COPY ./config ./config
COPY ./libraries ./libraries
COPY ./mods ./mods
COPY ./forge-* ./forge.jar
COPY ./minecraft_server.1.12.2.jar ./minecraft_server.1.12.2.jar
COPY ./server-icon.png ./server-icon.png
COPY ./banner.txt ./banner.txt

ENV VERSION=$VERSION

RUN echo "eula=true" > ./eula.txt
RUN echo "$VERSION" > ./version.txt

CMD ["--copy-server-properties"]