FROM ubuntu:20.04

WORKDIR /usr/src/app

RUN apt update && apt upgrade -y
RUN apt install curl -y

# Copy the hello.sh file from this location to /usr/src/app/ creating /usr/src/app/hello.sh
COPY script.sh .

# Alternatively, if we skipped chmod earlier, we can add execution permissions during the build.
RUN chmod +x script.sh

CMD ./script.sh 