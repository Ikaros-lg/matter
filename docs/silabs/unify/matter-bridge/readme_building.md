# Building the Unify Matter Bridge

This build guide cross-compiles for arm64 architecture to be run on Unify's reference platform - a Raspberry Pi 4 (RPi4) with the 64-bit version of Debian Bullseye.

## Check Out Submodules

Check out the necessary submodules with the following command.

```bash
dev-machine:~/matter$ ./scripts/checkout_submodules.py --platform linux
```

## Clone and Stage the Unify SDK Repository 

```bash
dev-machine:~/matter$ git clone --depth 1 https://github.com/SiliconLabs/UnifySDK.git --recursive ../uic-matter
```

## Build the Docker Container (arm64 compilation)

```bash
dev-machine:~/matter$ docker build -t unify-matter silabs_examples/unify-matter-common/docker/
```

## Run the docker container  (arm64 compilation)
