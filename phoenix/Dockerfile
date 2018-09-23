FROM elixir:1.7.3-alpine

# for alpine 3.8
ENV NODE_VERSION 9.11.1-r2
ENV NPM_VERSION 8.11.4-r0

RUN apk --update add --virtual build-dependencies wget build-base curl && \
    apk add nodejs-current=${NODE_VERSION} npm=${NPM_VERSION} bash && \
    apk del build-dependencies && \
    rm -rf /var/cache/apk/*

RUN mix local.hex --force && \
    mix archive.install --force https://github.com/phoenixframework/archives/raw/master/phx_new.ez && \
    mix local.rebar --force

WORKDIR /app
