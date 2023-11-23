# InexDroid #

### Sync ###

# Initialize local repository
```bash
repo init -u https://github.com/inex-droid/manifest -b tea
```

# Sync
```bash
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

### Build ###

# Set up environment
```bash
. build/envsetup.sh
```

# Choose a target
```bash
lunch aosp_$device-userdebug
```

# Build the code
```bash
mka bacon
```

### Credits ###
 * [**PixelExperience**](https://github.com/PixelExperience)
 * [**SkylineUI**](https://github.com/SkylineUI)
