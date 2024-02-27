
# Tutorial 

## Set up  

1. Download Unity Hub 

2. Through Unity Hub, download Unity 2022.3.17f1

3. [VR Overview Project Setup](https://docs.unity3d.com/Manual/VROverview.html)

    - Describes everything for Step 4

    - [Step by step tutorial](https://learn.unity.com/pathway/vr-development) for setting up a VR project in Unity

4. In Unity, from the menus select: 
Window > Package Manager > Install the following packages:
- Oculus XR Plugin
- TextMeshPro
- Unity UI
- Universal RP
- Universal RP Config
- XR Core Utilities 
- XR Interaction Toolkit
- XR Plugin Management
- Shader Graph

(You may need additional packages, but those additional ones probably come with the ones listed above)

5. Go to XR Plugin Management. Edit > Project Settings > XR Plugin Management.
    Under Android settings tab, check the box for Oculus under Plugin Provider, since we are using Meta Quest. 
    Under Occulus tab in the left sidebar, select Quest 2 as the target device. 

File > Build Settings > Switch from Windows, Mac, Linux to Android.

It will prompt you to change the project to Android. 

Switch "Run Device" to Meta Quest, after plugging the device into the computer. 

## Prefabs

## Code 

### 1. `LaunchProjectile.cs`

Goes with the blaster to shoot the bullets. 

Blaster predab has a start and attach point. The start point is where the bullet will be instantiated. The attach point is where the controller holds onto the blaster. 

`SerializeField` makes variable popup in the GUI. 

### 2. `Projectile.cs`

* Added 8 colors for bullets. 

* Picks one of 8 colors at random, at spawn. 

* Moves forward the projectile. 

    Handles collisions: increments score when bullet hits target object. 
    Decrements when bullet hits friendly object. 

### 3. `FollowCamera.cs`

* Makes the score user interface perpectually stay in front of the camera (in field of view). 

## Scene 

The scene is called "Range". All targets are prefabs. 