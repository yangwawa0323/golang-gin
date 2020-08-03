# Docker golang-gin 

This is a golang web framework

## Run the golang-gin docker

> Important: Mount Volume( your code folder) into container under the folder **/go/src/code**

```shell
docker run --name -d <instance_name> -v $(pwd):/go/src/code yangwawa0323/golang-gin
```
