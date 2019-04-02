VERSION=3.4.14
PROJECT_ID=k8szk
PROJECT=stardog/${PROJECT_ID}

all: build

build:
	docker build --pull -t ${PROJECT}:${VERSION} .

push: build
	docker push ${PROJECT}:${VERSION}

pushlatest: build
	docker tag ${PROJECT}:${VERSION} ${PROJECT}:latest
	docker push ${PROJECT}:latest

.PHONY: all build push
