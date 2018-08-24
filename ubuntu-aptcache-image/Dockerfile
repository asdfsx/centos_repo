FROM ubuntu:latest

RUN apt-get update &&\
    apt-get install -y apt-cacher-ng &&\
    rm -rf /var/lib/apt/lists/*

RUN sed 's/# ForeGround: 0/ForeGround: 1/' -i /etc/apt-cacher-ng/acng.conf

EXPOSE 3142

VOLUME ["/var/cache/apt-cacher-ng"]

CMD ["apt-cacher-ng", "-c", "/etc/apt-cacher-ng"]

