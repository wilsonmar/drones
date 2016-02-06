This article contains notes on making use of drones.

## The DJI Challenge
<a target="_blank" href="https://www.youtube.com/watch?v=_kXoUsqzzMU">
Video Introducing the SDK Challenge</a>

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

## Team Skills

Ford Touch interface: Richard Puckett
Image Recognition ML: Lance Hughes
Abhi Kolhe

Larissa Bemis
iOS app (React): Wilson Mar ?
Christopher Trudeau
# Development Schedule

### Mission Events Incremental MVPs 
A 50x50 meter arena = 164 feet
How high this is this? 
Watch this high dive https://www.youtube.com/watch?v=rEiwAAHakI0

#### In the final round/during competition:
Calibration (barometer for altitude)
GPS coordinates input (in a local file to start, max altitude for failsafe)
Calculate Flight path (for shortest mission time) given GPS.
Take-off command (from interactive display in the F150
RTH (Return to home)
Abort mission for manual piloting.
Chromecast or iOS AirPlay Mirroring for App broadcast
Stream video to cloud web server for the international press to watch ;)
Streaming live footage to the F150 (800 pixels wide by 384 pixels every 4 seconds)
Avoid obstacles (wind, go around )
Assimilating recordings (does it look like a survivor tag).
Recognize GPS coordinates
Abort landing.
Landing on ground
Landing on a moving vehicle

#### 1st round:
Input GPS coordinates from an interface

#### 2nd round:
Input GPS coordinates from an interface
DJI’s Manifold (portable computation platform) 
DJI’sX3 (4K gimbal mounted camera), 
DJI’s Guidance (5 directions of depth sensing)
Ford API Library and Emulator
Example AprilTags for objects and vehicle

#### Out of scope:
Wind resistance (as this is in an indoor arena)
## Team Members’ Responsibilities & Task Assignments

### Components:
ID recognition of “survivors” (http://people.csail.mit.edu/kaess/apriltags/)
ID recognition of “survivors” (http://people.csail.mit.edu/kaess/apriltags/)
DJI’s Matrice 100 (M100) flying platform, 
DJI’s Mobile SDK for iOS and Android, 
DJI’s Guidance SDK
DJI’s Onboard SDK
Battery chargers
"Mission timer stops when the M100 motors switch off.” so ideally the drone would power itself off.

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

# Reference Materials 

  has something changed in the picture since previous photos




## https://github.com/dji-sdk/

# Decisions:

### iPhone or Android?

iPhone needs to be plugged into the car with a USB cable; Android can do Bluetooth. Code in support for Chromecast, but AirPlay is free - that’s handled by the iPhone OS.

The M100 has a 40 minute fly time.
