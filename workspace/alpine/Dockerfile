FROM mhart/alpine-node
MAINTAINER Karl Li <killtw@gmail.com>

RUN apk add --update ruby ruby-dev libffi-dev build-base ruby-bundler \
    ca-certificates make musl build-base python python-dev py-pip && \
    pip install --upgrade pip && \
    echo 'gem: --no-rdoc --no-ri' > /etc/gemrc && \
    gem install sass compass && \
    apk del build-base libffi-dev ruby-dev && \
    npm set progress=false && \
    npm install --global --progress=false gulp bower webpack && \
    echo '{ "allow_root": true }' > /root/.bowerrc && \
    rm -rf /tmp/* && \
    rm -rf /var/cache/apk/* && \
    rm -r /root/.gem && \
    find / -name '*.gem' | xargs rm && \
    rm -rf /usr/share/ri

# VOLUME /workspace
WORKDIR /workspace
