# Local Manifests

These are local manifests for various devices.

Some of them may be broken, if they are dont hesitate to pull request.

If you have a working local manifest and want to add it here you can also pull request.

Generally spoken: if there is a rom that has a manifest, but is not released, the device trees are not buildable/bootable.

Some manifests have a similarly named .md file, which indicates the state of the trees, but it isnt updated regularly due to lack of time.


# Usage:
You can place the text in the .repo/local_manifests/manifest.xml after `repo init $SOME_ROM_MANIFEST_URL` by either:

manually creating .repo/local_manifests and a .xml file and then copying the code to .repo/local_manifests/manifest.xml.

OR

running
```
mkdir .repo/local_manifests
```
```
curl https://raw.githubusercontent.com/SirRGB/local_manifests/main/$DEVICE/$MANIFEST_NAME > .repo/local_manifests/manifest.xml
```
be sure to replace $DEVICE and $MANIFEST_NAME with a device codename and manifest name, that are available.

Example:
```
mkdir .repo/local_manifests && curl https://raw.githubusercontent.com/SirRGB/local_manifests/main/griffin/A11Lineage.xml > .repo/local_manifests/manifest.xml
```

after that do 
```repo sync --force-sync --no-tags --no-clone-bundle -c```
to get both the rom and device sources.
