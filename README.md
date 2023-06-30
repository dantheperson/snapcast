# snapcast

## Build Prerequisites
```
sudo apt-get install -y qemu-user-static
docker buildx create --use
docker buildx install
```

## Building
```
docker build --platform linux/amd64,linux/arm64,linux/riscv64,linux/arm,linux/amd64/v3 -t dantheperson/snapcast:server -f Dockerfile.server . --push 
docker build --platform linux/amd64,linux/arm64,linux/riscv64,linux/arm,linux/amd64/v3 -t dantheperson/snapcast:client -f Dockerfile.client . --push 
docker build --platform linux/amd64,linux/arm64,linux/riscv64,linux/arm,linux/amd64/v3 -t dantheperson/snapcast:latest -f Dockerfile . --push 
```
