FROM postgres:latest

RUN apt-get update
RUN apt-get install -y --force-yes build-essential wget git systemd lcov curl
RUN apt-get install -y --force-yes zlib1g-dev libssl-dev libreadline-dev libyaml-dev libxml2-dev libxslt-dev
RUN apt-get install -y --force-yes libboost-math-dev libboost-random-dev postgresql-server-dev-16 libpq-dev
RUN apt-get clean

USER postgres
RUN whoami
RUN /usr/lib/postgresql/16/bin/initdb
RUN git clone https://github.com/tarkmeper/numpgsql.git /build/numpgsql
git 