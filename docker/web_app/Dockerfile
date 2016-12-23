# Docker file for microbitpolska container
FROM python:3.6

# Upgrade System:
RUN apt-get update && \
 apt-get upgrade -y && \
 apt-get install -qq -y build-essential libssl-dev wget git

#Our Docker commands:
RUN mkdir -p /usr/src/microbitpolska.org
WORKDIR /usr/src/microbitpolska.org

RUN git clone https://github.com/MicrobitPolska/microbitpolskaorg.git .
RUN pip install -r requirements.txt