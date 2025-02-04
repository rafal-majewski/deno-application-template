ARG DENO_VERSION
FROM denoland/deno:alpine-${DENO_VERSION} AS development
WORKDIR /home/developer/deno-application-template
USER root
RUN apk add --no-cache git
RUN apk add --no-cache openssh
RUN deluser deno
RUN adduser -D developer
USER developer
# https://github.com/denoland/deno_docker/issues/373#issuecomment-2564164617
ENV LD_LIBRARY_PATH /usr/lib:/usr/local/lib
