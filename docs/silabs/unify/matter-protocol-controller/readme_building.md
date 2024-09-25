# Building the Unify Matter Protocol Controller

This build guide cross-compiles for arm64 architecture to be run on Unify's
reference platform - a Raspberry Pi 4 (RPi4) with the 64-bit version of Debian
Bullseye.

## Download and Stage the uic Repo

```bash
dev-machine:~$ git clone --depth 1 https://github.com/SiliconLabs/UnifySDK.git --recursive ../uic-matter
```

## Build the Docker Container (arm64 compilation)

```bash
dev-machine:~$ docker build -t unify-matter silabs_examples/unify-matter-common/docker/
```

Start the docker:

```bash
dev-machine:~$ docker run -it -v $PWD:/matter -v $PWD/../uic-matter:/uic unify-matter
```

## Build libunify

