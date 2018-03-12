.PHONY: build cluster test

default: build

build:
	go build -o bin/swarm    github.com/khs125/Clean-Slate-Shills/cmd/swarm
	go build -o bin/geth     github.com/khs125/Clean-Slate-Shills/cmd/geth
	go build -o bin/bootnode github.com/khs125/Clean-Slate-Shills/cmd/bootnode

cluster: build
	scripts/boot-cluster.sh

test:
	go test -v github.com/khs125/Clean-Slate-Shills/swarm/...
