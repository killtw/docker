FROM phusion/baseimage
MAINTAINER Karl Li <killtw@gmail.com>

RUN DEBIAN_FRONTEND=noninteractive && \
    locale-gen en_US.UTF-8

ENV LANGUAGE=en_US.UTF-8
ENV LC_ALL=en_US.UTF-8
ENV LC_CTYPE=UTF-8
ENV LANG=en_US.UTF-8
ENV TERM xterm

RUN add-apt-repository -y ppa:brightbox/ruby-ng && \
    curl -sL https://deb.nodesource.com/setup_5.x | bash - && \
    apt-get install -yq software-properties-common curl git build-essential nodejs ruby2.3 ruby2.3-dev&& \
    apt-get clean && \
    echo '{ "allow_root": true }' > /root/.bowerrc && \
    echo 'gem: --no-rdoc --no-ri' > /etc/gemrc && \
    npm set progress=false && \
    npm install -g webpack gulp bower && \
    gem install sass compass && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

WORKDIR /workspace
