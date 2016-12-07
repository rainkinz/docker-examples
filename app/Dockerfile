FROM ruby
MAINTAINER brendan <brendan.grainger@gmail.com>
EXPOSE 4567

WORKDIR /app

ENTRYPOINT ["bundle","exec","rackup","-p","4567","--host","0.0.0.0"]
ADD . /app
RUN bundle install
