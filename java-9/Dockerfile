FROM debian:stretch

MAINTAINER Chihab ASRIH <chihab.asrih@gmail.com>

RUN apt-get update && apt-get upgrade -y \
    && apt-get install -y gnupg gnupg2 gnupg1

# Add webupd8team repository
RUN echo "deb http://ppa.launchpad.net/webupd8team/java/ubuntu xenial main" | tee /etc/apt/sources.list.d/java.list \
    && echo "deb-src http://ppa.launchpad.net/webupd8team/java/ubuntu xenial main" | tee -a /etc/apt/sources.list.d/java.list \
    && apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys EEA14886

# Install Java 9
RUN apt-get update \
    && echo oracle-java9-installer shared/accepted-oracle-license-v1-1 select true | /usr/bin/debconf-set-selections \
    && echo debconf shared/accepted-oracle-license-v1-1 seen true | debconf-set-selections \
    && DEBIAN_FRONTEND=noninteractive apt-get install -y oracle-java9-installer oracle-java9-set-default

# Clean up
RUN rm -rf /var/cache/oracle-jdk9-installer /var/lib/apt/lists/* /tmp/* /var/tmp/* \
    && apt-get autoremove -y \
    && apt-get clean

# Define default command
CMD ["java"]