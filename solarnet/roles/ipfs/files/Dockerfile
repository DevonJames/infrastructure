FROM golang:1.4
MAINTAINER Brian Tiger Chow <btc@perfmode.com>

# This IPFS repo should be copied into ./go-ipfs
ADD go-ipfs /go/src/github.com/ipfs/go-ipfs

RUN cd /go/src/github.com/ipfs/go-ipfs/cmd/ipfs && go install

# clean up the image to keep it small
RUN rm -rf /go/src/github.com

EXPOSE 8080 4001 5001

CMD ["ipfs daemon"]
