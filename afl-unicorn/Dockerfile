FROM ubuntu:16.04
ARG VERSION=1

LABEL	maintainer="Andreia Ocanoaia andreia.ocanoaia@gmail.com" \
		name="Testing afl-unicorn" \
		version="${VERSION}"

WORKDIR /root

ENV DEBIAN_FRONTEND="noninteractive"

RUN apt-get update && \
	apt-get install -y wget vim git python python-pip python3 python3-pip automake autoconf \
	coreutils python-setuptools 

RUN git clone https://github.com/Battelle/afl-unicorn.git 

RUN ["/bin/bash", "-c", "pip install capstone"]

RUN ["/bin/bash", "-c", "cd /root/afl-unicorn && make && make install && cd /root/afl-unicorn/unicorn_mode && ./build_unicorn_support.sh"]

# CMD ["/bin/bash", "-c" "alf-fuzz -U -m none -i /root/afl-unicorn/unicorn_mode/samples/simple/sample_inputs -o /root/afl-unicorn/unicorn_mode/samples/simple/output -- python /root/afl-unicorn/unicorn_mode/samples/simple/simple_test_harness.py"]
