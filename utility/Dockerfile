####################################################
# Server Side Up -  Docker Utility Image
#####################################################
FROM docker:dind
LABEL maintainer="Jay Rogers <@jaydrogers>"

ARG COMPOSE_VERSION='v2.5.0'

# Install docker compose
RUN apk add --no-cache curl \
    && mkdir -p $HOME/.docker/cli-plugins \
    && curl -SL https://github.com/docker/compose/releases/download/${COMPOSE_VERSION}/docker-compose-linux-x86_64 -o $HOME/.docker/cli-plugins/docker-compose \
    && chmod 755 $HOME/.docker/cli-plugins/docker-compose \
    && rm -rf /var/cache/apk/*