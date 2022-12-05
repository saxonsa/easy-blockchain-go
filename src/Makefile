BINARY := blockchain

all: build test

build:
	@echo "==> Go build"
	@go build -o $(BINARY)

deps:
	@go get -u github.com/boltdb/bolt

test:
	./$(BINARY) printchain
	./$(BINARY) addblock -data "Send 1 BTC to Saxon"
	./$(BINARY) addblock -data "Pay 0.31337 BTC for Starbucks"
	./$(BINARY) printchain

.PHONY: build deps test
