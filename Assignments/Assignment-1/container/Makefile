IMG_NAME := slo-generator-rce
CONT_NAME := ${IMG_NAME}

build:
	docker build -t $(IMG_NAME) -f Dockerfile .

run: build
	docker run -it --name $(CONT_NAME) -t $(IMG_NAME) /bin/bash

stop:
	-docker stop $(CONT_NAME)

clean: stop
	-docker container rm $(CONT_NAME)
	-docker image rm $(IMG_NAME):latest

.PHONY: build run stop clean
