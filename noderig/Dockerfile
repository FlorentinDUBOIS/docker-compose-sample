FROM golang:alpine

RUN mkdir -p $GOPATH/src/github.com/runabove/noderig

WORKDIR $GOPATH/src/github.com/runabove/noderig

RUN apk add --update git curl glide
RUN git clone https://github.com/runabove/noderig . && glide install
COPY config.yaml /etc/noderig/config.yaml

CMD ["go", "run", "noderig.go"]
