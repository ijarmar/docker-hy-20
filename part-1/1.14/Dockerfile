FROM ubuntu:18.04

COPY . /app/rails
WORKDIR /app/rails

EXPOSE 3000

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y build-essential curl git libssl-dev libreadline-dev zlib1g-dev libsqlite3-dev tzdata

ENV PATH="/root/.rbenv/bin:${PATH}"
ENV PATH="/root/.rbenv/shims:${PATH}"

RUN curl -fsSL https://github.com/rbenv/rbenv-installer/raw/master/bin/rbenv-installer | bash
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash -
RUN apt-get install -y nodejs

RUN rbenv install 2.6.0

RUN gem install bundler && bundle install

RUN bundle exec rails db:migrate

#CMD ["rails", "s"]
CMD ["bundle", "exec", "rails", "s"]
