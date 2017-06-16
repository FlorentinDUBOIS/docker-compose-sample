FROM alpine

RUN apk add --update rust git openssl openssl-dev cargo
RUN mkdir -p /opt/beamium
WORKDIR /opt/beamium

RUN git clone https://github.com/runabove/beamium . && cargo build --release
COPY config.yml config.yml

CMD ["cargo", "run", "--release"]
