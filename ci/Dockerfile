FROM alpine:3.8
RUN apk add --no-cache darkhttpd
RUN mkdir /htdocs \
    && date | tee /htdocs/test.txt \
    && dd if=/dev/urandom of=/htdocs/random.bin count=1
EXPOSE 80
CMD ["/usr/bin/darkhttpd", "/htdocs", "--port", "80"]

