# Building AOSP for yogurt
# Local manifest
Just grab the manifest and sync to get device sources

```bash
curl -o .repo/local_manifests/local_manifests.xml https://raw.githubusercontent.com/vk401426/local_manifest/risingos/thirteen.xml --create-dirs



This guide provides instructions on building Android Open Source Project rising for yogurt.
 Follow these steps to set up the necessary repositories and build your custom ROM.

## Clone Required Repositories

### 1. Device Tree

Clone the device tree repository for [Device Name].

```sh
git clone -b risingos-13.0 https://github.com/vk401426/android_device_micromax_yogurt.git device/micromax/yogurt
```

### 2. Vendor Files

Clone the vendor files repository.

```sh
git clone -b lineage-20.0 https://github.com/vk401426/android_vendor_micromax_yogurt.git vendor/micromax/yogurt
```

### 3. Kernel Source

Clone the kernel source repository.

```sh
git clone -b android-13.0 https://github.com/vk401426/yogurt.git kernel/micromax/yogurt
```

### 4. Additional Components (Optional)

If needed, clone extra device-specific policies or other components.

```sh
git clone -b arrow-13.1 https://github.com/ArrowOS/android_device_mediatek_sepolicy_vndr.git device/mediatek/sepolicy_vndr
```

### 5. Google Apps (Optional)

Clone the GApps repository if you want to include Google Apps in your ROM.

```sh
git clone https://gitlab.com/arrowos-project/android_vendor_gapps.git vendor/gapps
```

## Build Process

Follow the official AOSP build instructions to build the ROM for your device.

```sh
. build/envsetup.sh
lunch aosp_[Device Name]-userdebug
make -j$(nproc)
```


## Contributing

If you find any issues or have improvements to suggest, feel free to create a pull request or raise an issue in this repository.

Happy building! 🚀
