DexProtector (https://dexprotector.com) is one of the **pioneers** in **mobile application and library shielding**. It protects and obfuscates Android and iOS applications and libraries. Our solution helps you to secure your code and assets against unauthorized or illegal use, tampering, reverse engineering, and cracking.

## Native Library Protection

This fork of Telegram is to demonstrate how Native Library Protection mechanism works.

## Description
https://dexprotector.com/docs#native-library-protection

## Requirements
- Android Studio or Gradle
- NDK
- DexProtector Enterpise with a valid license

## Configuring 
- Set path to Android SDK in local.properties
- Set path to DexProtector Enterprise in build.gradle (project’s root) instead of `/Users/developer/DexProtector`

## Building 
```
cd TMessagesProj/jni
<ndk-dir>/ndk-build
cd ..
gradle clean assembleRelease
```

## Evaluating
```
strings build/intermediates/jniLibs/x86/release/x86/libtmessages.22.so | grep AES- | wc -l
```
Expected output: **28**
```
unzip build/outputs/apk/TMessagesProj-x86-release.apk lib/x86/libtmessages.22.so
strings lib/x86/libtmessages.22.so | grep AES- | wc -l
```
Expected output: **0**

## Telegram messenger for Android

[Telegram](https://telegram.org) is a messaging app with a focus on speed and security. It’s superfast, simple and free.
This repo contains the official source code for [Telegram App for Android](https://play.google.com/store/apps/details?id=org.telegram.messenger).

##Creating your Telegram Application

We welcome all developers to use our API and source code to create applications on our platform.
There are several things we require from **all developers** for the moment.

1. [**Obtain your own api_id**](https://core.telegram.org/api/obtaining_api_id) for your application.
2. Please **do not** use the name Telegram for your app — or make sure your users understand that it is unofficial.
3. Kindly **do not** use our standard logo (white paper plane in a blue circle) as your app's logo.
3. Please study our [**security guidelines**](https://core.telegram.org/mtproto/security_guidelines) and take good care of your users' data and privacy.
4. Please remember to publish **your** code too in order to comply with the licences.

### API, Protocol documentation

Telegram API manuals: https://core.telegram.org/api

MTproto protocol manuals: https://core.telegram.org/mtproto

### Usage

**Beware of using the dev branch and uploading it to any markets, in many cases it not will work as expected**.

First of all, take a look at **src/main/java/org/telegram/messenger/BuildVars.java** and fill it with correct values.
Import the root folder into your IDE (tested on Android Studio), then run project.

### Localization

We moved all translations to https://www.transifex.com/projects/p/telegram/. Please use it.
