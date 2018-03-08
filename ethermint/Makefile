GOTOOLS := \
					 github.com/karalabe/xgo \
					 github.com/alecthomas/gometalinter

PACKAGES := $(shell glide novendor)

BUILD_TAGS? := ethermint

VERSION_TAG := 0.5.3

BUILD_FLAGS = -ldflags "-X github.com/tendermint/ethermint/version.GitCommit=`git rev-parse --short HEAD`"


### Development ###
all: get_vendor_deps install test

install:
	go install $(BUILD_FLAGS) ./cmd/ethermint

