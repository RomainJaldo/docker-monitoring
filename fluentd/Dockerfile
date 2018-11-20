# fluentd/Dockerfile

FROM fluent/fluentd:v1.3-debian

RUN apk add --no-cache --virtual .build-deps \
        git \
        ruby-dev \
        make \
        g++ \
    && \
    gem install fluent-plugin-elasticsearch && \
    gem sources --clear-all && \
    apk del .build-deps && \
    rm -rf /var/cache/apk/* /home/fluent/.gem/ruby/2.3.0/cache/*.gem