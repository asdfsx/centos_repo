FROM ubuntu:latest

ENV apngip repo

RUN echo 'Acquire::http::Proxy "http://'${apngip}':3142";' > /etc/apt/apt.conf.d/00proxy
#RUN sed -i "s/^deb http:\/\//deb http:\/\/${apngip}:3142\//g" /etc/apt/sources.list
#RUN sed -i "s/^deb-src http:\/\//deb-src http:\/\/${apngip}:3142\//g" /etc/apt/sources.list

