# E2fsprogs
It is repository of E2fsprogs (1.44.2) utility with instruction of building for Zynq SoC.

In current time, in *./build* directory already set all configs for Zynq ARM side (cortex-A9). 

In *./build/FINAL* you can find compiled sources and libraries for your Zynq.

The E2fsprogs - it is package containing the utilities for handlong the ext2 file system. It also supports the ext3 and ext4 journaling file system.

# HOWTO
For building with your cross-compiler, you need export next variables:

    export CROSS_COMPILE=arm-xilinx-linux-gnueabi-
    export ARCH=arm

Next step is preparing of compilation. In directory with E2fsprogs we create *build* directory and set configs:

    mkdir -v build
    cd build

    ../configure --host=arm-xilinx-linux-gnueabi --prefix=/usr --with-root-prefix="" --enable-elf-shlibs
	
    make
    make DESTDIR=<path to build execution sorces> install
    make DESTDIR=<path to build shared libraries> install-libs

# Useful links
[Instructions](http://www.linuxfromscratch.org/clfs/view/clfs-2.0/arm/final-system/e2fsprogs.html)

[Original repository](https://git.kernel.org/pub/scm/fs/ext2/e2fsprogs.git)


