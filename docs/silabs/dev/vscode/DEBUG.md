# Debugging in VS Code

This section covers remote debugging (GDB jlink) of Matter examples in VS Code.

## Requirements

1. C/C++ Extension Pack (_vscode extension_) - language support
2. Cortex-Debug (_vscode extension_) - GDB debugger support
3. ARM GCC Toolchain
   (https://developer.arm.com/open-source/gnu-toolchain/gnu-rm/downloads) -
   required arm-none-eabi tools
4. J-Link Software Tools - required J-Link GDB Server for J-Link based debuggers
   (https://www.segger.com/downloads/jlink)

## Settings

Before starting a debug session ensure the following:

