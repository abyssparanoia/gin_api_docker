FROM golang:1.9.2-alpine

COPY src/ /go/src/gin_test

WORKDIR /go/src/gin_test

RUN apk update \
    && apk add --no-cache git \
    && go get -u github.com/codegangsta/gin \
    && go get -u github.com/golang/dep/cmd/dep \
    && dep ensure

CMD gin -i run
