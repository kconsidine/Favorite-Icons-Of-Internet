GOCMD=go
GOBUILD=$(GOCMD) build
GOCLEAN=$(GOCMD) clean
GOINSTALL=$(GOCMD) install
GOTEST=$(GOCMD) test
GODEP=$(GOTEST) -i

export GOPATH:=$(CURDIR)/_vendor:$(CURDIR)/

APPNAME = gofavicon

all: clean build

clean:
	rm -rf bin

env:
	$(GOCMD) env

test:
	$(GOTEST) gofavicon gofavicon/cmd/crawlerd/

vet:
	$(GOCMD) vet

doc:
	godoc -http=":8080"

build:
	CGO_ENABLED=0 $(GOINSTALL) $(APPNAME)/...
