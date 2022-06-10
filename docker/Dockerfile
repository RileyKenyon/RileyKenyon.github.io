FROM ruby:3.0 AS jekyll-base

# throw errors if Gemfile has been modified since Gemfile.lock
RUN bundle config --global frozen 1

COPY . /root/website
WORKDIR /root/website

RUN bundle install

CMD [ "bundle", "exec", "jekyll", "serve", "--livereload" ]