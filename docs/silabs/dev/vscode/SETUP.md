# Set Up the VS Code environment

## General Requirements

1. Install Visual Studio Code for your operating system of choice here:
   https://code.visualstudio.com/Download
2. Install [Git](https://git-scm.com/) if you haven't already
3. _Windows Only_ Enable git to use LF instead of CLRF by default:
   `git config --global core.autocrlf false`
4. Git clone the Silicon Labs Matter repository here:
   https://github.com/SiliconLabs/matter
5. Launch Visual Studio Code, and open the cloned folder
6. When prompted to "install recommended extensions" please select "Install"
    - Recommended Extensions can be found
      [here](../../../../.vscode/extensions.json)
7. Ensure the following extensions are installed:
8. ARM GCC Toolchain
   (https://developer.arm.com/open-source/gnu-toolchain/gnu-rm/downloads) -
   required arm-none-eabi tools
9. J-Link Software Tools - required J-Link GDB Server for J-Link-based debuggers
   (https://www.segger.com/downloads/jlink)
10. Python - (https://www.python.org/downloads/)

### Installing prerequisites on macOS

On macOS, you must install Xcode from the Mac App Store. The remaining
dependencies can be installed and satisfied using [Brew](https://brew.sh/):

```shell
$ brew install openssl pkg-config
```

However, that does not expose the package to `pkg-config`. To fix that, run
something like the following:

Intel:

```shell
$ cd /usr/local/lib/pkgconfig ln -s ../../Cellar/openssl@1.1/1.1.1g/lib/pkgconfig/* .
```

where `openssl@1.1/1.1.1g` may need to be replaced with the actual version of
OpenSSL installed by Brew.

Apple Silicon:

```shell
$ export PKG_CONFIG_PATH=$PKG_CONFIG_PATH:"/opt/homebrew/opt/openssl@3/lib/pkgconfig"
```
