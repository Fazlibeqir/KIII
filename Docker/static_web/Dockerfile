FROM ubuntu:latest
WORKDIR /opt/webapp/db
RUN apt-get update && apt-get install -y \
    ruby-full \
    build-essential \
    libssl-dev \
    libreadline-dev \
    zlib1g-dev \
    && gem install bundler

RUN useradd -ms /bin/bash webappuser

COPY Gemfile Gemfile.lock /opt/webapp/db/

RUN bundle install
WORKDIR /opt/webapp
ENTRYPOINT ["rackup"]

