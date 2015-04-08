FROM jiangyong/docker-golang

RUN apk-install git 
RUN git config --global http.sslverify "false"

RUN go get github.com/mrwilson/helixdns && \
    go install github.com/mrwilson/helixdns

EXPOSE 53

CMD [ "helixdns", "-port", "53", "-etcd-address", "127.0.0.1:4001" ]
