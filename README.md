#### Prerequisites

1. Android SDK Tools 20.0.1
2. Android SDK Platform-tools 13
3. Android 4.1 API 16 SDK Platform 16.2
4. Android NDK r8b

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

#### Latin IME

    $ cd latinime
    $ ant debug
