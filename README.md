# Samsara
A rust operating system

## Prerequisites
This was built on windows, if you are not on windows you may need to adjust some things as needed. In the end it compiles to a baremetal x86_64 architecture regardless of host.

Set the rustup override to nightly:

`rustup override set nightly`

Add the rust-src component to allow core library recompiling:

`rustup component add rust-src`

## Building
to create a boot image:

install bootimage crate:

`rustup component add llvm-tools-preview`

`cargo install bootimage`

run `./build.bat`

If you need to change the target, do so in the .cargo/config.toml file

## Running
I am running with QEMU, I have QEMU in my PATH and I run the `./qemu.bat` script to run. Adjust the script to your needs/boot in another way