
1. How to Build
	- get Toolchain
		From android git server , codesourcery and etc ..
		 - arm-linux-androideabi-4.9

	- edit Makefile
		edit "CROSS_COMPILE" to right toolchain path(You downloaded).
		  EX)   CROSS_COMPILE= $(android platform directory you download)/android/prebuilts/gcc/linux-x86/aarch64/aarch64-linux-android-4.9/bin/
          Ex)   CROSS_COMPILE=/usr/local/toolchain/arm-linux-androideabi-4.9/bin/arm-linux-androideabi-          // check the location of toolchain
		  or
		  Ex)	export CROSS_COMPILE=arm-linux-androideabi-
		  Ex)	export PATH=$PATH:<toolchain_parent_dir>/arm-linux-androideabi-4.9/bin

		$ make ARCH=arm64 msm_defconfig
		$ make ARCH=arm64 zImage

2. Output files
	- Kernel : arch/arm64/boot/Image
	- module : drivers/*/*.