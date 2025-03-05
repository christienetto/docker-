FROM ubuntu:22.04

WORKDIR /usr/src/app

RUN apt-get update && apt-get install -y curl


COPY script.sh /script.sh


RUN chmod +x /script.sh


CMD ["bash", "/script.sh"]
