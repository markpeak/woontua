#### Information

    The original code was pulled from Android Jelly Bean source code (AOSP) by @sugree. The binary works for Android 4.1 and above.

    The master project is https://github.com/sugree/android-thaiime and this repo is an indirect fork from his repo.

    Thai dictionary is just a prove of concept implementation with *incomplete* word list. Need to improve in future versions.

#### Prerequisites

1. Android SDK Tools 20.0.1
2. Android SDK Platform-tools 13
3. Android 4.1 API 16 SDK Platform 16.2
4. Android NDK r8b

#### local.properties

    You need to add local.properties file in each directory with single configuration

    $ sdk.dir = [PATH to Android SDK]

#### Preparation

    $ mkdir latinime/libs

#### Library Compilation (one time)

    $ cd inputmethodcommon
    $ ant release
    $ cd ..
    $ cp inputmethodcommon/bin/classes.jar latinime/libs/inputmethodcommon.jar
    $ cd support-v4
    $ ant release
    $ cd ..
    $ cp support-v4/bin/classes.jar latinime/libs/android-support-v4.jar

#### Native Compilation

    $ cd latinime
    $ ndk-build
    $ cd ..

#### IME Compilation

    $ cd latinime
    $ ant debug

#### Testing Stage

    The compiled binaries will be located in latinime/bin. 
    Copy it to your Android environment using ADB. 
    Enabling it in Settings/Language.