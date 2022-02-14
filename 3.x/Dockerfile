FROM arm64v8/alpine:latest
LABEL maintainer="server@doveconviene.com"

RUN apk add --update --no-cache python3 git openssh-client python3-dev musl-dev linux-headers gcc libffi-dev && \
	python3 -m ensurepip && \
    pip3 install --upgrade pip && \
    pip3 install --upgrade --user awsebcli && \
    export PATH=~/.local/bin:$PATH

ENV PATH /root/.local/bin:$PATH
ENTRYPOINT ["eb"]
VOLUME ["/aws"]
WORKDIR /aws
