# RustSBI K210 Platform Support Package

This platform support package contains more platform compatibility functions, allowing the K210 to run the 1.12 version of the standard operating system kernel.

## binary package download

See the release page: [here](https://github.com/rustsbi/rustsbi-k210/releases)

## Instructions for use

Please download first [ktool.py](https://github.com/loboris/ktool), Placed in the `xtask` directory, that is, the file location is `xtask/ktool.py`.

Run the following commands to run the code directly on the target board.

```
cargo k210
```

This platform support package starts the OS kernel at `0x80020000` and provides a simple device tree in the `a1` register.
The operating system kernel should use version 1.12 of "RISC-V Instruction Set Architecture Volume II: Privileged Instructions" instead of version 1.9.1 supported by the chip.

## Compatibility documentation

Release later. Includes the `sfence.vma` directive, page exception number forwarding, and more.
## Try it now

Download the code first, then run the kernel tests directly:

```
cargo test
```

## Copyright Notice

The test framework of the project uses [KTool](https://github.com/loboris/ktool). This project is open sourced using the Apache 2.0 license, thanks to the KTool project and its maintainers!

Reference implementaion K210 includes Kendryte K210 DTS file from Western Digital, this file is
(C) Western Digital Corporation or its affiliates under BSD-2-Clause license.
