The objective is to create several stages of product that increase in useful capability over time 
(rather than individual components that can't do much unless assembled together at the end):

A. Mobile phone controlling Phantom 3 drone:

   0. Take-off command (from interactive display in the F150
   0. Abort mission button (to invoke manual piloting).

   0. Display video from drone on mobile app screen.
   0. Chromecast or iOS AirPlay Mirroring for App broadcast to a Google stick on HDMI of TV.
   0. Stream video to cloud web server for analysis and archival.
   0. Streaming live footage to the F150 (800x384 pixels every 4 seconds).
   
   0. GPS coordinates input (in a local file to start, max altitude for failsafe)
   0. RTH (Return to home) button
   1. Display mission log
   1. Display missions history

B. Image recognition and route planning/prioritization:

   0. AprilTag software on a Mac identity the position of AprilTag and dervive a value from image.
   0. Drone derive a value from AprilTag (http://people.csail.mit.edu/kaess/apriltags/)
   0. Identify <strong>GPS coordinates</strong> from a picture containing the recognized AprilTag

   0. Plot a straight course to the survivor coordinates (avoiding obstacles).
   0. Avoid obstacles (wind, go around ) in plotted course.
   0. Return to home (RTH) around known objects.
   0. Prioritize among several targets (for the quickest route).
   0. Landing on a moving vehicle

Along the way:

0. Calibration (barometer for altitude)
