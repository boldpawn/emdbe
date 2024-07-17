# EMDBE
"Events, my dear boy, events"

An Event Distribution System


### Usage in Go

Install protobuf
See https://grpc.io/docs/protoc-installation/

Install Go plugins for the protocol compiler:  
Install the protocol compiler plugins for Go using the following commands:
```
$ go install google.golang.org/protobuf/cmd/protoc-gen-go@v1.28
$ go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@v1.2
```

Update your PATH so that the protoc compiler can find the plugins:
```
$ export PATH="$PATH:$(go env GOPATH)/bin"

```

Generate the code
```
protoc --go_out=. --go_opt=paths=source_relative --go-grpc_out=. --go-grpc_opt=paths=source_relative emdbe.proto

```