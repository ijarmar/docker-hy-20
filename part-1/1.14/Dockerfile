FROM ruby:2.6.0
RUN apt-get update -qq && apt-get install -y nodejs

EXPOSE 3000

COPY . /app/rails
WORKDIR /app/rails

RUN gem install bundler && bundle install
RUN rails db:migrate

CMD ["rails", "s"]
