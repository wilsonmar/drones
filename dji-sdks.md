This article reviews DJI's SDKs on Github:

https://developer.dji.com/challenge2016/

* Kevin On – kevin.on@dji.com
* dev@dji.com

https://developer.dji.com/en/get-started/DJI-SDK-Structure/
describes the three SDKs working together or independently.

0. <a href="#MobileSDK">DJI’s Mobile SDK</a> for  for mobile devices to communicate with the flight controller's
    HD Live Video Feed，Intelligent Navigation and Flight Control
    on the DJI PC Simulator and Phantom 3, Inspire, and M100.

0. <a href="#OnboardSDK">DJI’s Onboard SDK</a> for 
   communication between on-board devices and the flight controller about
   Aircraft real time attitude control, transmitting sensors data
   on M100 only.

0. <a href="#GuidanceSDK">DJI’s Guidance SDK</a> uses on-board devices to retrieve data from 
   the DJI Guidance SDK to sense the surrounding environment for Ultrasonic Ranging,
   Binocular Obstacle Recognition on M100.

The language is C/C++.

<hr />
After going through registration for Airmap at https://developer.dji.com/

<a name="MobileSDK">
## Mobile SDK</a>
DJI's Mobile SDK at home page https://developer.dji.com/mobile-sdk/
consists of:

* Firmware for each DJI model (Phantom 3, Inspire 1, OSMO, 
* DJI PC Simulator Installer & User Manual
* WIN Driver Installer
* iOS SDK and SDK Sample and Release Notes
* Android SDK and SDK Sample and Release Notes for version 3.0.1 on Feb 4, 2016, update from 2.4)
 
http://developer.dji.com/mobile-sdk/documentation/
provides docs on classes, protocols, constants generated from code at
https://github.com/dji-sdk/Mobile-SDK-Android/tree/master/Sample%20Code

But more useful is
* https://developer.dji.com/en/get-started/mobile-sdk/Mobile-SDK-Features/

* https://developer.dji.com/en/get-started/mobile-sdk/Mobile-SDK-API-Introduction/
  contains color pictures of what is in DJI PC Simulator User Manual.pdf downloaded,
  except call-outs of flight data is transmitted to the PC through the UDP port 5566.
  The PC can interpret this data to create a virtual 3D environment for analysis.

Contributors include https://github.com/JonasVautherin
who also contributed to https://github.com/3drobotics/solodevguide
and http://code.opencv.org/projects/opencv/wiki
doing http://code.opencv.org/projects/opencv/wiki/FaceDetection
Gary Bradski, President and CEO, OpenCV Foundation

### DJI PC Simulator Installer
DJISimulator-Installer.exe
requires DJI_WIN_Driver_Installer.exe installed 
and does not run on Windows 10 (only to Windows 8.1).

http://www.dji.com/flysafe/no-fly



### Android_Mobile_SDK_3.0.1
0. Create an Android app and get the <strong>package</strong> ("com.dji.sdkdemo") from within
   AndroidManifest.xml' file.
0. Paste the key when creating the app at http://developer.dji.com/en/user/apps/#all
1. Open email from DJI with subject "Activate your app" and click the Activation link.
0. Click Save in the pop-up dialog. Click OK on the pop-up.
0. Copy the 24-digit hexadecimal App Key to your clipboard.



<hr />

<a name="OnboardSDK">
## Onboard SDK</a>
DJI’s Onboard SDK https://developer.dji.com/onboard-sdk/

A 256-digit hexadecimal communication key will be generated upon successfully Application created.


<hr />


<a name="GuidanceSDK">
## Guidance SDK</a>
DJI’s Guidance SDK


## Questions:
Switch from standard resolution to 4XHD

Waypoint Mission

How to analyze efficiency of flight path
Show trace on a 3D modeler also showing waypoints?




