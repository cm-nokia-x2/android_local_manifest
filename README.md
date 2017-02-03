Local manifest to build LineageOS 14.1 UNOFFICIAL for [Nokia X2 aka Ara](http://4pda.ru/forum/index.php?showtopic=651024)

How to build:
-------------

Initializing a Build Environment:

    https://source.android.com/source/initializing.html

Initialize repo:

    repo init -u git://github.com/LineageOS/android.git -b cm-14.1
    curl --create-dirs -L -o .repo/local_manifests/local_manifest.xml -O -L https://raw.githubusercontent.com/cm-nokia-x2/android_local_manifest/cm-14.1/local_manifest.xml
    repo sync


Compile:

    source ./build/envsetup.sh
    lunch cm_ara-userdebug
    make otapackage
