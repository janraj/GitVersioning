OWNER=XXX
VERSION_FILE="../version/VERSION"
version=1.0.0


.PHONY: build
build:

test:
	go test -v ../... -coverprofile=coverage.txt -covermode=atomic
	go tool cover -html=cp.out -o cover.html

publish:
	@echo 'Updating Version, and push image to quay'
	$(eval version = $(shell ./gitpush.sh | tail -1))
	@echo 'New versions $(version)'

clean:
         
