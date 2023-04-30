FROM ubuntu

LABEL maintainer="Prajwal Dhatwalia <dh.prajwal@gmail.com>"

USER root

# Copies files from outside the container to designated location within the container
COPY ./entrypoint.bash / 

RUN apt -y update
RUN apt -y install curl bash
RUN chmod 755 /entrypoint.bash

USER nobody

ENTRYPOINT [ "/entrypoint.bash" ]
