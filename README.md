# GearVR-UnrealEngine4
A simple game using Unreal Engine 4.11.2 for GearVR

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
3. [CodeWorks for Android](https://developer.nvidia.com/codeworks-android)

**Hardware**

1. A 2015 Samsung Galaxy phone i.e. S6, S6 edge, S6 edge+ or Note 5.
2. Samsung Gear VR.

### 2.3 Windows

**Software**

1. [Unreal Engine 4](https://www.unrealengine.com/dashboard)
2. [Android Studio](http://developer.android.com/sdk/index.html)
3. [CodeWorks for Android](https://developer.nvidia.com/codeworks-android)
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
  export PATH="/Users/akshayrajgollahalli/Library/Android/sdk/platform-tools:$PATH"
  export PATH="/Users/akshayrajgollahalli/Library/Android/sdk/tools:$PATH"
  ```
4. To save press `Control + x` and then press `y`.
3. Restart `Terminal` and type `android` to see if the tools are working.

### 3.2 Enabling Android Developer Options

1. Goto `Settings -> About -> Software Info` and click on `Build Number` **seven** times.
2. Now go back, You should now see `Developer Options`.

  <p align="center"><img src="https://raw.githubusercontent.com/akshaybabloo/GearVR-UnrealEngine4/master/Screenshots/DevOpti.png" alt="New Project" width="300"></p>

3. Click on `Developer Options` and enable `USB debugging`

  <p align="center"><img src="https://raw.githubusercontent.com/akshaybabloo/GearVR-UnrealEngine4/master/Screenshots/USBDebug.png" alt="New Project" width="300"></p>

4. Once you connect your phone to the system, it will ask you to confirm the connected computers RSA KEY. Click `Ok` to continue.
