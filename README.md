This SDK is for methink's android app test. 
This is a link to [한글](https://github.com/methinksBot/android-mtk-apptest/blob/main/README_ko.md) version


In your `build.gradle` or `build.gradle.kts`, please add dependency repositories,

# Setup

## 1. Add repositories
Make sure `NOT` to add to `buildscript` .

```
allprojects {
    repositories {
        ...
        google()
        mavenCentral()
        jcenter()
        maven {
            url = uri("https://jitpack.io")
        }
    }
}

```

## 2. Add dependency
Please find the latest release version. 

```
dependencies {
  implementation('com.github.methinksBot:android-mtk-apptest:latestVersion')
}
```

## 3. Set minSDK level and compile & target SDK level


```
  ...
  minSdk 24
  targetSdk 33
  compileSdk 33
  ...
```

# Initiate the SDK
Please contact your project manager to get `projectId` and other values for initialization
On your main activity's `onCreated()`

```
  MTKAppTestClient.initialize(this, "projectId" , isDebug = false, isInHouseProject = false)
```
