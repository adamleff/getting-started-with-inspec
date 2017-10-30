FROM alpine

RUN mkdir /share
RUN apk add --update build-base libxml2-dev libffi-dev ruby ruby-dev && \
    gem install --no-document inspec io-console && \
    apk del build-base
RUN echo "workstation is running" > /tmp/out
CMD ["/usr/bin/tail", "-f", "/tmp/out"]
