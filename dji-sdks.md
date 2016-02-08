This article are notes on how to make use of DJI's SDKs.

## Guidebook on Gitbook
The most handy starting point (I didn't see mentioned on DJI's website) is:
![A Githbook](https://dji-dev.gitbooks.io/mobile-sdk-tutorials/content/en/)
providing a tutorial with Disqus discussion threads (which no one seems to be using).
One of the chapters (Android Camera app) can't be reached, so look at 
the source for it is at https://github.com/dji-sdk/Mobile-SDK-Tutorial.
Get a pdf from https://www.gitbook.com/book/dji-dev/mobile-sdk-tutorials/details)


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




