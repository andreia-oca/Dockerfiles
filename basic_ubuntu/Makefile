version=0.1

build:
	docker image build -t my_ubuntu_img:${version} --build-arg VERSION=${version} .

run: build
	docker run -it --name ubuntu my_ubuntu_img:${version} /bin/bash

test: build
	docker run --rm --name ubuntu_tmp my_ubuntu_img:${version}

clean:
	docker rm -f ubuntu
	docker image rm my_ubuntu_img:${version}
