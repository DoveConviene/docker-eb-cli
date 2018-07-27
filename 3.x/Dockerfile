FROM alpine:latest
MAINTAINER DoveConviene <server@doveconviene.com>
RUN apk add --update --no-cache git python3 openssh-client && \
	python3 -m ensurepip && \
    pip3 install --upgrade pip && \
    pip3 install --upgrade --user awsebcli && \
    export PATH=~/.local/bin:$PATH

ENV PATH /root/.local/bin:$PATH
ENTRYPOINT ["eb"]
VOLUME ["/aws"]
WORKDIR /aws
