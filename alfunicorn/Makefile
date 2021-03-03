version=0.1

build:
	docker image build -t aflunicorn_img:${version} --build-arg VERSION=${version} .

run: build
	docker run -it --name aflunicorn aflunicorn_img:${version} /bin/bash

clean:
	docker rm -f aflunicorn

clean_all:
	docker rm -f aflunicorn
	docker image rm aflunicorn_img:${version}
