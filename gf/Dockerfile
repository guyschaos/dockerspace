FROM alpine
ARG VERSION=1.3.0a
RUN mkdir /gf && cd /gf && \
    wget https://github.com/coyove/goflyway/releases/download/${VERSION}/goflyway_linux_amd64.tar.gz && \
    tar xvzf goflyway_linux_amd64.tar.gz && rm goflyway_linux_amd64.tar.gz && chmod +x goflyway
RUN mkdir /data
WORKDIR /gf
VOLUME ["/data"]

CMD ./goflyway ${OPTS}