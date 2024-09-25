# Building the Unify Matter Bridge for Debian Bullseye (Or similar Ubuntu) x86_64 

In the following subsections the commands should either be run on your local development machine or inside a running Docker container, as distinguished by the structure of the example.

## Set Up the Matter Build Environment

Once you have all the necessary submodules, source the Matter environment with the following command. This loads a number of build tools and makes sure the correct toolchains and compilers are used for compiling the Unify Matter Bridge.

## Check Out Submodules

Check out the necessary submodules with the following command.

```bash
dev-machine:~/matter$ ./scripts/checkout_submodules.py --platform linux
```

## Clone and Stage the Unify SDK Repository 