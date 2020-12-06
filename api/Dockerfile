# Use an official Ruby runtime as a parent image
FROM ruby:2.5.7

RUN printf "deb http://archive.debian.org/debian/ jessie main\ndeb-src http://archive.debian.org/debian/ jessie main\ndeb http://security.debian.org jessie/updates main\ndeb-src http://security.debian.org jessie/updates main" > /etc/apt/sources.list
RUN apt-get update -qq && apt-get install -y nodejs postgresql-client
# Set the working directory to /myapp
RUN mkdir /api
WORKDIR /api
COPY Gemfile /api/Gemfile
COPY Gemfile.lock /api/Gemfile.lock
RUN gem install bundler -v 2.1.4
RUN bundle install
# Copy the current directory contents into the container at /myapp
COPY . /api
# Add a script to be executed every time the container starts.COPY entrypoint.sh /usr/bin/
EXPOSE 3000
