# hermes-twrp-omni
Redmi note 2 twrp device tree (test version with 6.0 roms support)

# How to build
```
repo init --depth=1 -u git://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni.git -b twrp-6.0

mkdir -p .repo/local_manifests

wget -O .repo/local_manifests/local_manifests.xml http://raw.githubusercontent.com/bjsiu/hermes-twrp-test/master/local_manifests.xml

repo sync -j4

source build/envsetup.sh

lunch omni_hermes-eng

make -j4 clobber && make -j4 recoveryimage
```

# Current Bugs
1. Battery XX% jumps (bug of 6.0 kernel)
2. 'Reboot bootloader' is fixed on this version (prebuilt kernel version still not be fixed)

# License
Apache License v2.0 (for all files expert kernel source)
