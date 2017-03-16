# hermes-twrp-omni
Redmi note 2 twrp device tree

# How to build
```
repo init --depth=1 -u git://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni.git -b twrp-6.0

mkdir -p .repo/local_manifests

wget -O .repo/local_manifests/local_manifests.xml http://raw.githubusercontent.com/bjsiu/hermes-twrp-omni/master/local_manifests.xml

repo sync -j4

source build/envsetup.sh

lunch omni_hermes-eng

make -j4 clobber && make -j4 recoveryimage
```

# Current Bugs
1. maybe some sepolicy conflict but seems not effect to normal use, IDK
2. 'Reboot Bootloader' is not working

# License
Apache License v2.0 (for all files)
