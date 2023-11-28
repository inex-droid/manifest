![InexDroid](https://raw.githubusercontent.com/inex-droid/manifest/tea/inexdroid.png)


Requirements
------------------------------------------------------
- Around `500GB` disk space.
- Around `18GB` RAM running Linux.
------------------------------------------------------
As a first step, you'll have to create and enter a folder with the appropriate name.
To do that, run these commands:
------------------------------------------------------
```bash
   mkdir inex
   cd inex
```

To initialize your local repository, run this command:
------------------------------------------------------
```bash
repo init -u https://github.com/inexdroid/manifest -b tea
```

To save bandwith and space, run this command:
------------------------------------------------------
```bash
repo init --depth=1 --no-repo-verify -u https://github.com/inexdroid/manifest -b tea -g default,-mips,-darwin,-notdefault
```

Afterwards, sync the source by running this command:
------------------------------------------------------
```bash
repo sync -c --no-clone-bundle --no-tags --optimized-fetch --prune --force-sync -j8
```

:hammer: Building
---------------

In case you are building Mac OS X, you are required to install coreutils from MacPorts before you continue. In order to build, use this command:
------------------------------------------------------
```bash
. build/envsetup.sh
```
------------------------------------------------------
```bash
lunch aosp_$device-userdebug
```
------------------------------------------------------
```bash
mka bacon
```
------------------------------------------------------
:dove: Credits:
 * [**crdroid**](https://github.com/crdroidandroid)
 * [**PixelExperience**](https://github.com/PixelExperience)
 * [**SkylineUI**](https://github.com/SkylineUI)
