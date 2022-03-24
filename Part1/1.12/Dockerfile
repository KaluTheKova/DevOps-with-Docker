FROM debian:buster-slim

# Curl
RUN apt update && apt upgrade && apt install curl -y

# Required installs
RUN curl -sL https://deb.nodesource.com/setup_16.x | bash
RUN apt install -y nodejs

# Building
WORKDIR /usr/src/app
COPY . .
RUN ls

RUN npm install
RUN node -v && npm -v

RUN npm run build
RUN npm install -g serve
EXPOSE 5000

RUN ls

CMD ["serve", "-s", "-l", "5000", "build"]

# docker run -it -p 127.0.0.1:5000:5000 example-frontend