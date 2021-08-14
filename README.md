Read at first: https://github.com/nguyenanhgiau/local_manifests/tree/rpi4-a12-telephony
# Build Android
Apply [the patch fix for android-s-beta-2](https://github.com/android-rpi/device_arpi_rpi4/wiki/arpi-12-:-framework-patch)<br>
Run the below command for building AOSP:

```bash
cd <aosp_dir>
source build/envsetup.sh
lunch rpi4-eng
make ramdisk systemimage vendorimage -j[n]
```
Use -j[n] option with make, if build host has a good number of CPU cores.

# Build Kernel
There is a prebuild kernel image in scripts/kernel-android-S.<br>
If you want to build a custom kernel, follow [building kernel](https://github.com/android-rpi/kernel_manifest)

# Prepare sd card
We provide a script in $ANDROID_BUILD_TOP/scripts for writing and packaging.
Follow [Android4Pi Script](https://github.com/nguyenanhgiau/a4rpi-scripts)

