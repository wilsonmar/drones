# Development Plan
<img align="right" alt="agile mvp" src="https://cloud.githubusercontent.com/assets/300046/12909852/f64315f0-ceb9-11e5-8540-0c0046047881.jpg">
The objective is to create several useful intermediate products over time, each with increasing capability
(rather than individual components that can't do much unless assembled together at the end):

<a href="#PhantomCapabilities">
A. Control Phantom 3 drone</a>

<a href="#M100Capabilities">
B. Control M100 drone</a>

<a href="#ImageRecognition">
C. Image recognition</a>

<a href="#RoutePlanning">
D. Route planning/prioritization</a>

<a href="#ServerCapabilities">
E. Server (may be out of scope)</a>


<a name="PhantomCapabilities">
## A. Control Phantom 3 drone</a>
The progress of computer control is similar to how a human gradually learns to fly safely -- gradually taking more risk of damaging equipment as skills increase.

   0. Display video from drone on mobile app screen.
   0. Chromecast or iOS AirPlay Mirroring for App broadcast to a Google stick on HDMI of TV.
   0. Streaming live footage to the F150 (800x384 pixels every 4 seconds).
   0. Stream video to cloud web server for analysis and archival. [OUT OF SCOPE]
   0. GPS coordinates input (in a local file to start, max altitude for failsafe)

   0. Simulator display actual mission log, etc.
   0. Simulator store coordinates with keywords.

   0. Take-off command (from interactive display in the F150
   0. Abort mission button (to invoke manual piloting) immediately.
   0. RTH (Return to home) button after short missions.
   0. Really store coordinates with keywords.

<a name="M100Capabilities">
## B. Controll M100 drone</a>

   0. Insert in accessory bay.
   0. Occipital sensor detects ceiling height.
   0. TensorFlow loaded, receives input.
   1. TensorFlow communicate with drone.
   2. Map Minecraft

<a name="ImageRecognition">
## C. Image recognition</a>

   0. AprilTag software on a Mac identity the position of AprilTag and dervive a value from image.
   0. Drone derive a value from AprilTag (http://people.csail.mit.edu/kaess/apriltags/)
   0. Identify <strong>GPS coordinates</strong> from a picture containing the recognized AprilTag

<a name="RoutePlanning">
## D. Route planning/prioritization</a>

   0. Coordinates to on-board computer for short mission.
   0. Initial take-off.
   1. Abort landing from smartphone controller.
   0. Return to home (RTH) around known objects.

   0. Plot a straight course to the survivor coordinates (avoiding obstacles).
   0. Avoid obstacles (wind, go around ) in plotted course.
   0. Prioritize among several targets (for the quickest route).
   0. Landing on a moving vehicle

<a name="ServerCapabilities">
## E. Server (out of scope)</a>

   0. Archival of video and photos (media assets)
   1. Retrieval of individual media assets
   2. Comparison of differences in media of same area over time
   3. Issue alert if differences are significant enough
   0. Identify what areas have been covered and what needs coverage
   1. Generate coverage map display
   0. Plan missions 
   1. Prioritize missions
   2. Maintain history of missions by drones and battery use (for predictive maintenance)

Along the way:

0. Calibration (barometer for altitude)
