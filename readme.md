# README

source: https://hub.docker.com/_/ruby

# Generate a Gemfile.lock
The above example Dockerfile expects a Gemfile.lock in your app directory. This docker run will help you generate one. Run it in the root of your app, next to the Gemfile:

$ docker run --rm -v "$PWD":/usr/src/app -w /usr/src/app ruby:2.7.2 bundle install

# Steps
$ docker build -t my-ruby-app .
$ docker run -it --name my-running-script my-ruby-app