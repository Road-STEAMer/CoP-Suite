FROM ruby:3.0.0
LABEL maintainer="ivan@platoniq.net"

ENV LANG C.UTF-8
ENV LC_ALL C.UTF-8

WORKDIR /code

RUN apt-get install -y git imagemagick wget \
  && apt-get clean

RUN curl -sL https://deb.nodesource.com/setup_14.x | bash - \
  && apt-get install -y nodejs \
  && apt-get install -y postgresql-client \
  && apt-get clean

RUN npm install yarn -g

RUN npm install -g npm@6.3.0
RUN gem install bundler
#RUN gem install doorkeeper -v 5.6.2
RUN gem install decidim



ENV RAILS_ENV=development
ENV PORT=3000

COPY Gemfile Gemfile.lock ./
#RUN bundle update marcel
#RUN bundle update mimemagic
#RUN bundle update mime-types



RUN bundle install
COPY . .
RUN bundle install
RUN bundle exec rails webpacker:install
RUN bundle exec rake assets:precompile