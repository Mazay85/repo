# Cortex Readme

## System Requirements
### ubuntu
Cortex node is developed in Ubuntu 18.04 x64 + CUDA 9.2 + NVIDIA Driver 396.37 environment, with CUDA Compute capability >= 6.1. Latest Ubuntu distributions are also compatible, but not fully tested.
Recommend:
- cmake 3.11.0+
 ```
wget https://cmake.org/files/v3.11/cmake-3.11.0-rc4-Linux-x86_64.tar.gz
tar zxvf cmake-3.11.0-rc4-Linux-x86_64.tar.gz
sudo mv cmake-3.11.0-rc4-Linux-x86_64  /opt/cmake-3.11
sudo ln -sf /opt/cmake-3.11/bin/*  /usr/bin/
 ```
- go 1.10.0+
```
wget https://dl.google.com/go/go1.11.5.linux-amd64.tar.gz
sudo tar -C /usr/local -xzf go1.11.5.linux-amd64.tar.gz
echo 'export PATH="$PATH:/usr/local/go/bin"' >> ~/.bashrc
source ~/.bashrc
```
- gcc/g++ 5.4+
```
sudo apt install gcc
```
- cuda 9.2+ (if u have gpu)
```
export LD_LIBRARY_PATH=/usr/local/cuda/lib64/:/usr/local/cuda/lib64/stubs:$LD_LIBRARY_PATH
export LIBRARY_PATH=/usr/local/cuda/lib64/:/usr/local/cuda/lib64/stubs:$LIBRARY_PATH
```
- nvidia driver 396.37+
- ubuntu 16.04+
### centos
Recommend:
- cmake 3.11.0+
```
yum install -y gcc gcc-c++ make automake 
yum install -y wget
wget https://cmake.org/files/v3.12/cmake-3.12.0-rc1.tar.gz
tar -zxvf cmake-3.12.0-rc1.tar.gz
cd cmake-3.12.0-rc1
./bootstrap
gmake
gmake install
```
- go 1.10.0+
- gcc/g++ 5.4+
- cuda 10.1+ (if u have gpu)
```
export LD_LIBRARY_PATH=/usr/local/cuda/lib64/:/usr/local/cuda/lib64/stubs:$LD_LIBRARY_PATH
export LIBRARY_PATH=/usr/local/cuda/lib64/:/usr/local/cuda/lib64/stubs:$LIBRARY_PATH
```
- nvidia driver 418.67+
- centos 7.6

## Cortex Full Node

### Compile Source Code And Run
see https://github.com/CortexFoundation/CortexTheseus/blob/dev/README.md

### Running Bash

And then, run any command to start full node `cortex`:

```Bash
1. cd cortex
2. export LD_LIBRARY_PATH=./:$LD_LIBRARY_PATH
3. ./build/bin/cortex --infer.devicetype=cpu/gpu
```


