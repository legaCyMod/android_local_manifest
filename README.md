Local manifests to build CyanogenMod 10.1 for [ZTE Blade](http://www.modaco.com/topic/359832-cyanogenmod-10.1), [ZTE Blade III](http://www.modaco.com/topic/360987-cyanogenmod-10.1) and [ZTE V9](http://www.modaco.com/topic/361573-cyanogenmod-10.1).

How to build:
-------------

Initialize repo:

    repo init -u git://github.com/CyanogenMod/android.git -b cm-10.1
    curl --create-dirs -L -o .repo/local_manifests/local_manifest.xml -O -L https://raw.github.com/legaCyMod/android_local_manifest/cm-10.1/local_manifest.xml
    repo sync

### Blade:

    curl -L -o .repo/local_manifests/manifest_zte_blade.xml -O -L https://raw.github.com/legaCyMod/android_local_manifest/cm-10.1/manifest_zte_blade.xml
    repo sync

Compile:

    . build/envsetup.sh
    brunch blade

### Blade III:

    curl -L -o .repo/local_manifests/manifest_zte_atlas40.xml -O -L https://raw.github.com/legaCyMod/android_local_manifest/cm-10.1/manifest_zte_atlas40.xml
    curl -L -o .repo/local_manifests/manifest_bluez.xml -O -L https://raw.github.com/legaCyMod/android_local_manifest/cm-10.1/manifest_bluez.xml
    repo sync

Compile:

    . build/envsetup.sh
    brunch atlas40

### V9:

    curl -L -o .repo/local_manifests/manifest_zte_v9.xml -O -L https://raw.github.com/legaCyMod/android_local_manifest/cm-10.1/manifest_zte_v9.xml
    repo sync

Compile:

    . build/envsetup.sh
    brunch v9

