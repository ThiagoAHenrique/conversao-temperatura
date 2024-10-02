FROM ubuntu
ARG NODE_MAJOR=20
RUN apt-get update
RUN apt-get install curl -y
RUN curl -fsSL https://deb.nodesource.com/setup_22.x -o nodesource_setup.sh
RUN bash nodesource_setup.sh
RUN apt-get install nodejs -y
WORKDIR /app
COPY . /app/
RUN npm install
ENTRYPOINT [ "node","server.js" ]
