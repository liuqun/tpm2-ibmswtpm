# Build Under Fedora 28
## Install requirements
```
sudo dnf install gcc make patch openssl-devel
```
## Build
```
make -C src
```

# Build Under Ubuntu 16.04 LTS
## Install snapcraft
```
sudo apt-get install -y snapcraft
```
## Build
```
snapcraft
```
## Result
Copy prime/tpm\_server to /usr/local/bin/ or anywhere else.
