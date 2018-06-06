FROM alpine:latest
MAINTAINER DoveConviene <server@doveconviene.com>
RUN apk add --update --no-cache python py-pip git openssh-client && \
    pip install --upgrade pip && \
    pip install --upgrade --user awsebcli && \
    export PATH=~/.local/bin:$PATH

ENV PATH /root/.local/bin:$PATH
ENTRYPOINT ["eb"]
VOLUME ["/aws"]
WORKDIR /aws
