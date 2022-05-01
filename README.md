#### device_oneplus_billie2
had to make couple tweaks
#### TWRP 10 for OnePlus Nord N100

## Requirements

You'll need to install repo - the app not the git object

``` sudo apt-get install repo ```

## How to build

### Create dirs
``` mkdir tw; cd tw ```

### Init repo

``` sudo repo init --depth=1 -u https://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni.git -b twrp-10.0-deprecated ```

### Clone guam repo

``` git clone https://github.com/ters55/device_oneplus_billie2 -b main device/oneplus/billie2 ```

### Sync

``` sudo repo sync --no-repo-verify -c --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -j`nproc` ```

### Build

``` source build/envsetup.sh; lunch omni_billie2-eng; mka recoveryimage` ```


Credits
* betaxab/contributors: For ginna device tree base
