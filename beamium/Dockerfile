FROM alpine:latest

RUN apk add --update rust git openssl openssl-dev cargo
RUN mkdir -p /opt/beamium
WORKDIR /opt/beamium

RUN git clone https://github.com/runabove/beamium . && cargo build --release
COPY config.yaml config.yaml

CMD ["cargo", "run", "--release"]
