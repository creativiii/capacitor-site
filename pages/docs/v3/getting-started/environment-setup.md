---
title: Environment Setup
description: Setting up a development environment for Capacitor
contributors:
  - mlynch
  - dotNetkow
---

# Environment Setup

Capacitor has a number of dependencies depending on which platforms you're targeting and which operating systems you are developing on.

## Requirements

You will need at least [NodeJS 12 LTS](https://nodejs.org) or later to get started. For specific platforms, follow each guide below to ensure you have the correct dependencies installed.

### Running your App

To run your app on hardware and virtual devices, you will need to install [`native-run`](https://github.com/ionic-team/native-run/):

```bash
npm install -g native-run
```

## iOS Development

To build iOS apps, you will need **macOS**. You will also need to download and set up [Xcode](https://developer.apple.com/xcode/).

> [Ionic Appflow](http://ionicframework.com/appflow) can be used to perform iOS cloud builds if you don't have a Mac.

### CocoaPods

Install [CocoaPods](https://cocoapods.org/), which is used to manage Capacitor packages for iOS.

```bash
sudo gem install cocoapods
```

### Xcode Command Line Tools

Install the **Xcode Command Line Tools** by opening **Xcode -> Preferences -> Locations** and selecting the latest version in the dropdown.

![Xcode locations preferences](/assets/img/docs/ios/xcode-preferences-location.png)

## Android Development

To build Android apps, you will need to download and set up [Android Studio](https://developer.android.com/studio/index.html).

### Android SDK

Developing Android apps requires some Android SDK packages to be installed. Make sure to install the Android SDK Tools, and a version of the Android SDK Platforms for API 21 or greater.

In Android Studio open **Tools -> SDK Manager** from the menu and install the platform versions you'd like to test with in the **SDK Platforms** tab:

![SDK Platforms](/assets/img/docs/android/sdk-platforms.png)

In the **SDK Tools** tab, make sure to install at least the following:

* Android SDK Build-Tools
* Android Emulator
* Android SDK Platform-Tools
* Android SDK Tools

![SDK Tools](/assets/img/docs/android/sdk-tools.png)

> You can use [`native-run`](https://github.com/ionic-team/native-run) to check the health of your Android SDK installation and look for missing packages:
>
> ```bash
> native-run android --sdk-info
> ```