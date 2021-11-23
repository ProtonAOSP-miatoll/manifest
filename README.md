# ProtonAOSP

ProtonAOSP is a minimal custom Android ROM focused on UI/UX and performance, with a touch of security and privacy. It is based on [Android Open Source Project (AOSP)](https://source.android.com/).

## Initializing Repo

First, make sure you have an [Android build environment](https://source.android.com/setup/build/initializing) and the [repo tool](https://source.android.com/setup/build/downloading) set up. After that, run the following commands:

```bash
# Install Repo in the created directory
$ repo init -u https://github.com/ProtonAOSP/android_manifest -b sc

# Time to sync
$ repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

This is a large download that will take approximately 100 GB of disk space, so plan accordingly.

## Building

```bash
# Set up environment
$ . build/envsetup.sh

# Choose a target
$ lunch device-userdebug

# Building target
$ make proton -jX
```

You will need to create/adapt a device tree to build this ROM for your device.

Good luck!
