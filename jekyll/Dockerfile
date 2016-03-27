# Docker for Jekyll 
FROM alpine:latest
MAINTAINER Hadi Hariri <mail@hadihariri.com>

# Install base stuff
RUN apk update && apk upgrade && apk add curl wget bash

# Install Ruby, Headers, etc. and export path
RUN apk add ruby ruby-bundler ruby-dev ruby-irb ruby-rdoc libatomic readline readline-dev \
    libxml2 libxml2-dev libxslt libxslt-dev zlib-dev zlib \
    libffi-dev build-base git nodejs \
    && export PATH="/root/.rbenv/bin:$PATH"

# Cleanup after apk
RUN rm -rf /var/cache/apk/*

# Install Jekyll and required gems
RUN gem install jekyll redcarpet kramdown maruku rdiscount RedCloth liquid pygments.rb \
    jekyll-paginate jekyll-sass-converter

