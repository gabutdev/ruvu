FROM ruby:2.6.6
RUN apt-get update -qq && apt-get install -y postgresql-client

ENV APP /api
RUN mkdir $APP
WORKDIR $APP
COPY Gemfile* $APP/
RUN mkdir -p $APP/log && touch $APP/log/development.log
RUN gem install bundler
RUN bundle install
COPY . $APP
RUN gem install foreman
