# heroku-docker

Simple image based on `node:latest` which adds Heroku CLI and Docker.

Dockerfile:

    FROM node:latest

    RUN npm install -g heroku
    RUN wget -qO- https://get.docker.com/ | sh

    ENTRYPOINT ["/bin/sh"]
