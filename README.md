# Use Github Actions to compile Custom Recovery
```
Supports TWRP, OrangeFox, PBRP & SHRP compilation and production
```
---

## Release Notes
```
= 2024-03-05
- [TWRP, OrangeFox] Allow non-Github/Gitlab remotes for AOSP device trees




-----

## Parameter Description
(not all branches require/support all of the below fields)

| Name | Description | Example |
| ------------ | -------------------- | ------------ |
| `MANIFEST_BRANCH` | Source branch | 12.1 |
| `DEVICE_TREE_URL` | Device tree address | https://github.com/TeamWin/android_device_asus_I003D |
| `DEVICE_TREE_BRANCH` | Device branch that you want to use for build (typically corresponds to the manifest branch) | android-12.1 |
| `DEVICE_PATH` | Device tree location for syncing, relative to workspace root (usually listed as "LOCAL_PATH" or "DEVICE_PATH" in BoardConfig.mk) | device/asus/I003D |
| `DEVICE_NAME` | Model name (same as twrp_`<DEVICE_NAME>`.mk from device tree) | I003D |
| `DEVICE_MAKEFILE` | Name of device-specific makefile from tree (format: `<PREFIX>_<DEVICE_NAME>`) | twrp_I003D
| `REPOPICK_PATCHES` | (Optional) Gerrit patches to include in build (space separated) - if you don't know what this means, then leave blank | 1245 1437 |
| `BUILD_TARGET` | Build Target Partition (boot/recovery/vendor_boot) | recovery |
| `RECOVERY_INSTALLER` | Include recovery installer zip | no |
| `OPTIONAL_FLAGS` | Additional/custom build commands should be entered here | export FOX_VIRTUAL_AB_DEVICE=1 |

-----

## Usage Instructions
```
For example, your username is: Run-114514
```
#### 1. Click 'Fork' in the upper right corner of this repo
![](https://i.bmp.ovh/imgs/2021/10/6b6ed9f29e732372.png)
#### 2. After waiting for the automatic redirection, you will see your own username
![](https://i.bmp.ovh/imgs/2021/10/66cfe324c0ebb69b.png)
## Building the Recovery
#### 3. Click 'Actions-Recovery Build'
![](https://i.bmp.ovh/imgs/2021/10/23896d1b66292047.png)
#### 4. Click 'Run workflow', choose the branch for the recovery that you want to build, and fill in according to the above 'Parameter Description'
![](https://i.bmp.ovh/imgs/2021/10/9cb7871267cf2f53.png)
#### 5. After filling in, click 'Run workflow' to start running

-----

## Compilation results
Can be downloaded at [Release](../../releases)

-----
## Reference

#### TeamWin Recovery Project: https://github.com/minimal-manifest-twrp
#### OrangeFox Recovery: https://gitlab.com/OrangeFox/sync.git
#### PitchBlack Recovery Project: https://github.com/PitchBlackRecoveryProject/manifest_pb.git
#### SKYHAWK Recovery Project: https://github.com/SHRP/manifest.git
