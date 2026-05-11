
# NixOS for i.MX (7)

This repo details an attempt to create a cross-compilation environment from x86_64 NixOS to the Toradex iMX7 SOM.
The main use case is compiling C++ using the QtCreator IDE.


### Building

The C++ toolchain is based on the Toradex BSP and SDK. Nix requires that it be wrapped and stored as derivations. The toolchain's `sysroot` filesystem is not native to NixOS, but the SOM itself will be running a FHS compliant OS.

`qtcreator` needs to be run in a shell with lots of environment variables set. We currently use an old version that is built using Qt5.
