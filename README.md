# GearVR-UnrealEngine4
A simple game using Unreal Engine 4.11.2 for GearVR

> Note 1: For Mac users make sure you download Java 6 -> [https://support.apple.com/kb/dl1572](https://support.apple.com/kb/dl1572) and Java 7.

**Table of content**

- [1 Introduction](#1-introduction)
- [2 Requirements](#2-requirements)
	- [2.1 General](#21-general)
	- [2.2 Mac](#22-mac)
	- [2.3 Windows](#23-windows)
- [3 Instillation](#3-instillation)
	- [3.1 Mac](#31-mac)
		- [3.1.1 Android Studio](#311-android-studio)
	- [3.2 Enabling Android Developer Options](#32-enabling-android-developer-options)
	- [3.3 Getting device ID](#33-getting-device-id)
	- [3.4 Downloading `Oculus Signature File (osig)` and placing it in UE](#34-downloading-oculus-signature-file-osig-and-placing-it-in-ue)
	- [3.4 Installing `CodeWorks for Android`](#34-installing-codeworks-for-android)
- [4 Developing a game](#4-developing-a-game)
- [5 Packing it up for Android](#5-packing-it-up-for-android)
	- [5.1 Package Configuration](#51-package-configuration)
	- [5.2 Packing](#52-packing)

## 1 Introduction

In this tutorial I will be going to develop a simple environment where the first person player can walk around. This game was developed in Mac and should be similar to windows. Please see "Note" where I would be including some important points about the structure and running of the game.

## 2 Requirements

### 2.1 General

1. A 2015 Samsung Galaxy phone i.e. S6, S6 edge, S6 edge+ or Note 5.
2. Samsung Gear VR.
3. Experience with Unreal Engine 4. If you don't have any previous experience, you can go through my tutorial on Unreal Engine 4 [here](https://github.com/akshaybabloo/UnrealEngine_4_Notes)

### 2.2 Mac

**Software**

1. [Unreal Engine 4](https://www.unrealengine.com/dashboard)
2. [Android Studio](http://developer.android.com/sdk/index.html)
3. AndroidWorks

**Hardware**

1. A 2015 Samsung Galaxy phone i.e. S6, S6 edge, S6 edge+ or Note 5.
2. Samsung Gear VR.

### 2.3 Windows

**Software**

1. [Unreal Engine 4](https://www.unrealengine.com/dashboard)
2. [Android Studio](http://developer.android.com/sdk/index.html)
3. AndroidWorks
4. Samsung drivers

**Hardware**

1. A 2015 Samsung Galaxy phone i.e. S6, S6 edge, S6 edge+ or Note 5.
2. Samsung Gear VR.

## 3 Instillation

### 3.1 Mac

#### 3.1.1 Android Studio

1. Download [Android Studio](http://developer.android.com/sdk/index.html).
2. Open it and move it to `Application`.
3. Open the application and follow the instillation process.
4. Once the instillation process is done open the application and do the follow
  1. Click on `Android Studio -> Preference`
  2. Click on `Appreance & Behavior -> System Settings -> Android SDK` and tick on `Android 5.0.1` and `Android 5.1.1`.

**Installing command line tools**

1. Open `Terminal`.
2. Type `nano .bash_profile` and type the following in it:

  ```shell
  # Android
  export PATH="/Users/<user>/Library/Android/sdk/platform-tools:$PATH"
  export PATH="/Users/<user>/Library/Android/sdk/tools:$PATH"
  ```

  > Note 2: `<user>` should be replaced by your user name.

4. To save press `Control + x` and then press `y`.
3. Restart `Terminal` and type `android` to see if the tools are working.

### 3.2 Enabling Android Developer Options

1. Goto `Settings -> About -> Software Info` and click on `Build Number` **seven** times.
2. Now go back, You should now see `Developer Options`.

  <p align="center"><img src="https://raw.githubusercontent.com/akshaybabloo/GearVR-UnrealEngine4/master/Screenshots/DevOpti.png" alt="New Project" width="300"></p>

3. Click on `Developer Options` and enable `USB debugging`

  <p align="center"><img src="https://raw.githubusercontent.com/akshaybabloo/GearVR-UnrealEngine4/master/Screenshots/USBDebug.png" alt="New Project" width="300"></p>

4. Once you connect your phone to the system, it will ask you to confirm the connected computers RSA KEY. Click `Ok` to continue.

### 3.3 Getting device ID

Make sure you have your phone connected to the computer and the `USB debugging` is switched on. Open `Terminal` and type in `adb devices`. This will print of an alpha numeric/numeric key something like this.

```
List of devices attached
1234567891011123	device
```

### 3.4 Downloading `Oculus Signature File (osig)` and placing it in UE

Copy the above number and goto [https://developer.oculus.com/osig/](https://developer.oculus.com/osig/) and paste it in the text field then click on `Download File`. `oculussig_1234567891011123` file will be downloaded.

Move this file to `/Users/Shared/UnrealEngine/4.10/Engine/Build/Android/Java/assets/`

### 3.4 Installing `CodeWorks for Android`

Goto `/Users/Shared/UnrealEngine/4.10/Engine/Extras/AndroidWorks/Mac/`. Open `AndroidWorks-1R1-osx.dmg` and follow the instillation steps.

This is what I have installed:

```
The following components are installed:
Android SDK
    +Android SDK Base 24.2.0
    +Android Platform Tools 22.0.0
    +Android Build Tools 22.0.1
    +Android 4.4.2(API 19) 4.4.2
    +Android 5.0 (API 21) 5.0.1
    +Android SDK Support Library 22.2.0
    +Android SDK Support Repository Library 15
Android Toolchain
    +Android NDK 10e
    +Apache Ant 1.8.2
    +Gradle 2.2.1
```

## 4 Developing a game

Please see my tutorial on [UnrealEngine 4](https://github.com/akshaybabloo/UnrealEngine_4_Notes).

> Note 2: The game developed in this tutorial is only a sample environment generated by UnrealEngine.

## 5 Packing it up for Android

### 5.1 Package Configuration

Once you have completed designing the game do the following:

Open `Plugins`

<p align="center"><img src="https://raw.githubusercontent.com/akshaybabloo/GearVR-UnrealEngine4/master/Screenshots/Plugins.png" alt="New Project" width="700"></p>

Then, make sure you have enabled the following:

<p align="center"><img src="https://raw.githubusercontent.com/akshaybabloo/GearVR-UnrealEngine4/master/Screenshots/Plugins1.png" alt="New Project" width="700"></p>


Next open your `Project Settings...`

<p align="center"><img src="https://raw.githubusercontent.com/akshaybabloo/GearVR-UnrealEngine4/master/Screenshots/ProjectSettingsMenu.png" alt="New Project" width="700"></p>

Then do the following:

<p align="center"><img src="https://raw.githubusercontent.com/akshaybabloo/GearVR-UnrealEngine4/master/Screenshots/AndroidPlatform.png" alt="New Project" width="700"></p>

Then do this:

<p align="center"><img src="https://raw.githubusercontent.com/akshaybabloo/GearVR-UnrealEngine4/master/Screenshots/AndroidPlatform1.png" alt="New Project" width="700"></p>

And then this:

<p align="center"><img src="https://raw.githubusercontent.com/akshaybabloo/GearVR-UnrealEngine4/master/Screenshots/AndroidPlatformSDK.png" alt="New Project" width="700"></p>

### 5.2 Packing

Do the following:

<p align="center"><img src="https://raw.githubusercontent.com/akshaybabloo/GearVR-UnrealEngine4/master/Screenshots/Packing.png" alt="New Project" width="700"></p>
