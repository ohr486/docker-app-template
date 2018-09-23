FROM ruby:2.5.1-alpine3.7

RUN apk --update add --virtual build-dependencies wget curl && \
    apk add nodejs build-base mysql-dev zlib-dev libxml2-dev libxslt-dev tzdata yaml-dev bash && \
    apk del build-dependencies && \
    rm -rf /var/cache/apk/*

RUN gem install bundler

WORKDIR /tmp
ADD app/Gemfile Gemfile
ADD Gemfile.lock Gemfile.lock
RUN bundle install

ENV APP_HOME /app
WORKDIR /app
