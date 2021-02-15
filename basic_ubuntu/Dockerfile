FROM ubuntu:20.04
ARG VERSION=1

LABEL	maintainer="Andreia Ocanoaia andreia.ocanoaia@gmail.com" \
		name="Basic Ubuntu" \
		version="${VERSION}"

WORKDIR /root

ENV DEBIAN_FRONTEND="noninteractive"
RUN apt-get update && \
	apt-get install -y iputils-ping net-tools iproute2 wget \
	git ssh vim dsniff curl tcpdump nmap driftnet iptables

CMD echo -ne "Hello world!\n"
