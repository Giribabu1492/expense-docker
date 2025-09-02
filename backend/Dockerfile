FROM node:20
WORKDIR /opt/backend
COPY package.json .
COPY *.js .
RUN npm install
ENV DB_HOST="mysql"
CMD [ "node", "index.js" ]

FROM debian:bookworm

RUN apt-get update && \
    apt-get install -y telnet netcat && \
    rm -rf /var/lib/apt/lists/*
