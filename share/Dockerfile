FROM ubuntu:18.04
RUN cd /home
RUN apt-get update && apt-get install -y gnupg2 binutils-common binutils make wget gcc libssl-dev libcurl3 git autoconf automake libtool groff-base perl m4
RUN git clone https://github.com/curl/curl.git
RUN cd curl && autoreconf -fi && ./configure --with-openssl && make && make install && ldconfig && curl -V
CMD tail -f /dev/null