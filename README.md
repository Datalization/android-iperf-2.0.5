Iperf-2.0.5 for Android
=======================
Requirements

1) Iperf - Version 2.0.5
2) Android NDK - Version r8b

Iperf-2.0.5: https://github.com/downloads/thangam-arunx/android-iperf-2.0.5/iperf.2.0.5.zip

Android NDK: http://developer.android.com/tools/sdk/ndk/index.html


How to build using android ndk r8b ??
=====================================

Follow this instrcution to compile iperf 2.0.5 for using Android NDK 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
export NDK_HOME="~/android-ndk-r8b"

mkdir $NDK_HOME/apps -p

cd $NDK_HOME/apps

unzip iperf.2.0.5.zip

cd $NDK_HOME

export "CC=$NDK_HOME/toolchains/arm-linux-androideabi-4.4.3/prebuilt/linux-x86/bin/arm-linux-androideabi-gcc --sysroot=$NDK_HOME/platforms/android-9/arch-arm"

make APP=iperf
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Executable: $NDK_HOMEapps/iperf/project/libs/armeabi/iperf
Any issues, Please leave comment.


How to run it on Android ??
===========================

adb push apps/iperf/project/libs/armeabi/iperf /data/local/tmp/
adb shell chmod 755 /data/local/tmp/iperf

:-)


