FROM golang:alpine

RUN mkdir -p $GOPATH/src/github.com/runabove/noderig

WORKDIR $GOPATH/src/github.com/runabove/noderig

RUN apk add --update git curl glide tzdata
RUN ln -sf /usr/share/zoneinfo/Europe/Paris /etc/localtime
RUN git clone https://github.com/runabove/noderig . && glide install
COPY config.yaml /etc/noderig/config.yaml

CMD ["go", "run", "noderig.go"]
