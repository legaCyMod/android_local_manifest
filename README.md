Local manifests to build CyanogenMod 11 for [ZTE Blade III](http://www.modaco.com/topic/367241-cyanogenmod-11/), [ZTE Open C / Kis 3](http://www.modaco.com/topic/373214-devrom148-cyanogenmod-11-android-444/) and Motorola Moto G.

How to build:
-------------

Initialize repo:

    repo init -u git://github.com/CyanogenMod/android.git -b cm-11.0
    curl --create-dirs -L -o .repo/local_manifests/local_manifest.xml -O -L https://raw.githubusercontent.com/legaCyMod/android_local_manifest/cm-11.0/local_manifest.xml
    repo sync

### ZTE Blade III:

    curl -L -o .repo/local_manifests/manifest_zte_atlas40.xml -O -L https://raw.githubusercontent.com/legaCyMod/android_local_manifest/cm-11.0/manifest_zte_atlas40.xml
    repo sync

Compile:

    . build/envsetup.sh
    brunch atlas40

### ZTE Open C / Kis 3:

    curl -L -o .repo/local_manifests/manifest_zte_kis3.xml -O -L https://raw.githubusercontent.com/legaCyMod/android_local_manifest/cm-11.0/manifest_zte_kis3.xml
    repo sync

Compile:

    . build/envsetup.sh
    brunch kis3

### Motorola Moto G:

    curl -L -o .repo/local_manifests/manifest_motorola_falcon.xml -O -L https://raw.githubusercontent.com/legaCyMod/android_local_manifest/cm-11.0/manifest_motorola_falcon.xml
    repo sync

Compile:

    . build/envsetup.sh
    brunch falcon
