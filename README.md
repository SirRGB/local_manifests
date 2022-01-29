# Local Manifests

These are my local manifests for various devices.

Some of them may be broken, if they are dont hesitate to pull request.

If you have a working local manifest and want to add it here you can also pull request.

Generall spoken: if there is a rom that has a manifest, but is not released, the device trees are not buildable/bootable.


# Usage:
You can place the text in the .repo/local_manifests/manifest.xml after `repo init $SOME_ROM_MANIFEST_URL` by either:

manually creating .repo/local_manifests and file and then copying the code to .repo/local_manifests/manifest.xml

OR

running
```
mkdir .repo/local_manifests
curl https://raw.githubusercontent.com/SirRGB/local_manifests/main/$DEVICE/$MANIFEST_NAME > .repo/local_manifests/manifest.xml
```
be sure to replace $DEVICE and $MANIFEST_NAME with a device codename and manifest name, that are available

Example:
```
mkdir .repo/local_manifests && curl https://raw.githubusercontent.com/SirRGB/local_manifests/main/griffin/A11Lineage.xml > .repo/local_manifests/manifest.xml
```

after that do `repo sync --force-sync --no-tags --no-clone-bundle -c`
