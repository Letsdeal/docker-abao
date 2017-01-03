FROM node:6.9.2

RUN apt-get update && apt-get install -y wget

ENV DOCKERIZE_VERSION v0.3.0
RUN wget https://github.com/jwilder/dockerize/releases/download/$DOCKERIZE_VERSION/dockerize-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
    && tar -C /usr/local/bin -xzvf dockerize-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
    && rm dockerize-linux-amd64-$DOCKERIZE_VERSION.tar.gz

RUN npm install -g abao@0.5.0

RUN mkdir -p /data
VOLUME /data
WORKDIR /data

ENTRYPOINT ["abao"]

CMD ["--help"]
