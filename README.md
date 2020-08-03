# Docker golang-gin 

This is a golang web framework

## Run the golang-gin docker

> Important: Mount Volume( your code folder) into container under the folder **/go/src/code**

```shell
docker run --name -d <instance_name> -v $(pwd):/go/src/code yangwawa0323/golang-gin
```

## Manual install go package

Manual install go package in the docker golang container, this has already done. Just for memory what is done for golang orginal image.


```shell
root@91dfd823aeb3:/go/src/code# history
  # set git low speed limit
  git config --global http.lowSpeedLimit 0
  git config --global http.lowSpeedTime 999999

  # Using gitclone mirror of github.com
  git config --global url."https://gitclone.com/github.com".insteadOf https://github.com

  # Get sys
  git clone https://github.com/golang/sys golang.org/x/sys

  # Get go-cmp v0.4.0
  git clone  https://github.com/google/go-cmp   google/go-cmp/v0.4.0
  
  # protobuf-go , not protobuf 
  git clone https://github.com/protocolbuffers/protobuf-go google.golang.org/protobuf
   
  git clone https://github.com/golang/sys golang.org/x/sys
  
  go get github.com/gin-gonic/gin

  # Put your code under /go/src/code
  cd code/
  go run start.go

  # Clear cache
  rm /root/.cache/ -rf

```
