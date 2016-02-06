This article contains notes on making use of drones.

## DJI
<a target="_blank" href="http://www.dji.com/">DJI</a>
has great image stabilization and ease-of-flying technologies.

* http://www.facebook.com/DJIGlobal  
* http://www.twitter.com/DJIGlobal  
* http://www.youtube.com/DJI

### The DJI Challenge
<a target="_blank" href="https://www.youtube.com/watch?v=_kXoUsqzzMU">
Video Introducing the SDK Challenge</a>

![drone dji developer challenge arena](https://cloud.githubusercontent.com/assets/300046/12867343/d4bb8442-cc9f-11e5-8b78-720c7e0cf464.jpg)

![drone-on-truck](https://cloud.githubusercontent.com/assets/300046/12867256/81a776a0-cc9d-11e5-9a44-43f086b546c1.png)

![drone-f150-sync-dash-menu](https://cloud.githubusercontent.com/assets/300046/12867279/36fa7750-cc9e-11e5-860a-1a1dc193bdce.png)

Felix Tian

http://accelerate.im/challenges

http://accelerate.im/events/12

OSMO is a revolutionary handheld camera that helps you record videos and take photos, stabilizing the camera no matter how you move it. Find out more about this camera here: http://www.dji.com/product/osmo. We challenge you to build an amazing mobile app for DJI Osmo using our Mobile SDK.
The winning team will receive a $3,000 cash award plus one DJI Osmo for each team member (up to five).


## Development Plan:

Pluses (tabled for now)
Hover over an area?
Mobile device communicate with 
Image recognition server
Image recognition on-board drone
Tasking (assign flight patch coordinates among drones for shortest mission time)
Database to house images
Database software to receive images (Riak?)
Charging

Questions:
A) How is the 50 x 50m delimited? Yes, with GPS coordinates but also recognizable visible physical boundaries too?

---------------

# Proposal

# Development Plan

# Technical Feasibility Analysis

# Development Schedule

### Mission Events Incremental MVPs 
A 50x50 meter arena = 164 feet How high this is this? 
   Watch a high dive: https://www.youtube.com/watch?v=rEiwAAHakI0

#### In the final round/during competition:
0. Calibration (barometer for altitude)
0. GPS coordinates input (in a local file to start, max altitude for failsafe)
0. Calculate Flight path (for shortest mission time) given GPS.
0. Take-off command (from interactive display in the F150
0. RTH (Return to home)
0. Abort mission for manual piloting.
0. Chromecast or iOS AirPlay Mirroring for App broadcast
0. Stream video to cloud web server for the international press to watch ;)
0. Streaming live footage to the F150 (800 pixels wide by 384 pixels every 4 seconds)
0. Avoid obstacles (wind, go around )
0. Assimilating recordings (does it look like a survivor tag).
0. Recognize GPS coordinates
0. Abort landing.
0. Landing on ground
0. Landing on a moving vehicle

#### 1st round:

#### 2nd round:
0. Input GPS coordinates from an interface
0. DJI’s Manifold (portable computation platform) 
0. DJI’sX3 (4K gimbal mounted camera), 
0. DJI’s Guidance (5 directions of depth sensing)
0. Ford API Library and Emulator
0. Example AprilTags for objects and vehicle

#### Out of scope:
0. Wind resistance (as this is in an indoor arena)
0. ID recognition of “survivors” (http://people.csail.mit.edu/kaess/apriltags/)

# Components from DJI:
0. DJI’s Matrice 100 (M100) flying platform, 
0. DJI’s Mobile SDK for iOS and Android, 
0. DJI’s Guidance SDK
0. DJI’s Onboard SDK
0. Battery chargers
0. "Mission timer stops when the M100 motors switch off.” so ideally the drone would power itself off.

### mobile app components:
Connection status with drone
Video feed from camera
Self-test results?
Take-off button
Abort button
Return home
Mission timer
Mission History 
Connection status with F150 Touch screen
Connection status with server
### Ford screen (subset) https://www.ford.com/technology/sync/

Map
Button “Abort” "Return home”
http://blog.caranddriver.com/first-touch-we-sample-fords-sync-3-interface-and-it-doesnt-suck/
http://owner.ford.com/how-tos/sync-technology/all/sync-applink/use-voice-commands-to-control-your-smartphone-apps.html
Voice commands

  has something changed in the picture since previous photos


## https://github.com/dji-sdk/

# Decisions:

### iPhone or Android?

iPhone needs to be plugged into the car with a USB cable; Android can do Bluetooth. Code in support for Chromecast, but AirPlay is free - that’s handled by the iPhone OS.

The M100 has a 40 minute fly time.

## Team Members’ Responsibilities & Task Assignments
* Ford SYNC Touch interface: Richard Puckett
* Image Recognition ML: Lance Hughes
* Abhi Kolhe
* Larissa Bemis
* iOS app (React): Wilson Mar ?
* Christopher Trudeau

# Reference Materials 

