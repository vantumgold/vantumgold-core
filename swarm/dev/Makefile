.PHONY: build cluster test

default: build

build:
	go build -o bin/swarm    github.com/vntg-project/vntg/cmd/swarm
	go build -o bin/geth     github.com/vntg-project/vntg/cmd/geth
	go build -o bin/bootnode github.com/vntg-project/vntg/cmd/bootnode

cluster: build
	scripts/boot-cluster.sh

test:
	go test -v github.com/vntg-project/vntg/swarm/...
