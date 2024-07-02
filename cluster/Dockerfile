FROM bde2020/hadoop-namenode:2.0.0-hadoop2.7.4-java8

RUN rm /etc/apt/sources.list
RUN echo "deb http://archive.debian.org/debian/ jessie main" | tee -a /etc/apt/sources.list
RUN echo "deb-src http://archive.debian.org/debian/ jessie main" | tee -a /etc/apt/sources.list
RUN echo "Acquire::Check-Valid-Until false;" | tee -a /etc/apt/apt.conf.d/10-nocheckvalid
RUN echo 'Package: *\nPin: origin "archive.debian.org"\nPin-Priority: 500' | tee -a /etc/apt/preferences.d/10-archive-pin

RUN apt-get update
RUN apt-get install python3 -y --force-yes