
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

0. ZenMuse X3 is the camera.
0. Manifold is the "High performance computing designed for the DJI Onboard SDK to bring true intelligence to flying platforms."
0. Guidance is for visual sensing 

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

https://developer.ford.com/
https://developer.ford.com/pages/applink/
https://developer.ford.com/pages/ale (AppLink™Emulator) software emulator
