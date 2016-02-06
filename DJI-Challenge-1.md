
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

Since time is of the essence, a strategy is needed which minimizes:

  A. the risk of running into obstacles and

  B. the likelihood of finding survivors with the minimum effort.

STRATEGY 1: Flying vertically up and down would avoid obstacles better that across the field.

STRATEGY 2: The drone has a high resolution camera, so we want to leverage that.
Upon takeoff, the drone first flies high over the middle of the field to be at a high vantage point for 
taking a hi-res overview picture used to identify objects and prioritize waypoints.
"Conventional" approaches (such as the CNN Google uses) are based on the 2-dimentional pictures.

STRATEGY 3: The server issues a list of possible targets, 
sorted by highest likelihood, which the drone flies to in order. 

Pictures from the drone would go through the mobile phone which receives and forwards media from the drone to the server.

STRATEGY 4: Images taken are saved on a server's database for comparison across time,
and to use for the basis of additional learning.

STRATEGY 5: There is a chance that the server is slow in coming back with a list.
In case that happens, the drone then circles the perimeter of its mission field 
to take pictures at different angles which provide a better chance of detecting objects,
hoping that the better granularity closer to objects may improve image recognition.

STRATEGY 6: The pictures are used by the server to construct a 3D model of the terrain and obstacles.

STRAGEGY 7: On its way, the drone takes pictures of what’s enroute, building a full catalog of the field.
Each image is geo coded.

STRATEGY 8: Before each flight, the drone's altimeter and other sensors are calibrated to ensure accuracy
needed to better compare data across different days and drone units.

Beyond the scope of this current set is operation of multiple drones at the same time.



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
