[TOC]

# Android device-mark

Android ALog provides :
- ~~Full method count 00~~

Less Runtime :
- minSdkVersion 9
- gradle or maven
- jar [You can Download just like this Path]((https://github.com/MDL-Sinlov/MDL-Android-Repo/raw/master/mvn-repo/mdl/sinlov/android/))

> eclipse just use every repo at version `device-mark-x.x.x-jarLib.jar`

Project Runtime:
- Android Studio 2.2
- appcompat-v7:23.4.0
- Gradle 2.14.1
- com.android.tools.build:gradle:2.2.0
- minSdkVersion 15

# Last Version Info

- version 0.1.2
- repo at https://github.com/MDL-Sinlov/MDL-Android-Repo

# Demo

[Download Demo at Android-Device-Mark-debug-0.1.2.apk](https://github.com/MDL-Sinlov/MDL_Android-Device-Mark/raw/master/Apk-For-Test/Android-Device-Mark-debug-0.1.2.apk)

# Dependency

at root project `build.gradle`

```gradle
repositories {
    maven {
        url 'https://raw.githubusercontent.com/MDL-Sinlov/MDL-Android-Repo/master/mvn-repo/'
    }
    jcenter()
    ...
}
```

in module `build.gradle`

```gradle
dependencies {
    compile 'mdl.sinlov.android:device-mark:0.1.2'
}
```

# Usage

- need permission

```xml
    <uses-permission android:name="android.permission.ACCESS_WIFI_STATE" />
    <uses-permission android:name="android.permission.READ_PHONE_STATE" />
    <uses-permission android:name="android.permission.INTERNET" />
```


```java
# you can use MAC from API9 - API23
String mac = "mac:\n" + DeviceIDFactory.getDeviceIDByMac();
# if full use of get MAC addr
String macSafe = "macSafe:\n" + DeviceIDFactory.getDeviceIDByMac(aCtx);

# Full of API can use like install UUID
String uuid = "uuid:\n" + DeviceIDFactory.getUUID(aCtx);

# match deivceID by wifi imei UUID
String deviceId = "deviceID:\n" + DeviceIDFactory.getDeviceId(aCtx, "");
```


###License

---

Copyright 2017 sinlovgm@gmail.com

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
