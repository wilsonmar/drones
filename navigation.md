# Navigation 
This page describes the strategies core to the Challenge.

<a href="#Takeoff">Take-off</a> > <a href="#FlightPlan">Search Route</a> > <a href="#ImageAcquisition">Image Acquisition</a> -> <a href="#TargetID">Target Identification</a> > <a href="#RTH">Return</a> > <a href="#Landing">Landing</a>

QUESTION: Are these the stages?


<a name="Takeoff">
## Take-off</a>
Before take-off, there is a built-in automatic check for no-fly zone.

STRATEGY: <strong>Fast take-off</strong> to avoid air disturbance of the support vehicle and to maximize time.

The vehicle knows which direction to begin based on coordinates keyed in prior to takeoff.

The landscape is akin to a maze. There will be some dead-ends requiring back-tracking.

QUESTION: A basic pattern of flight needs to be selected.

STRATEGY a: <strong>Start from center then circle out?</strong>

STRATEGY b: <strong>Start from a corner?</strong>

STRATEGY c: <strong>Random?</strong> Maybe it doesn't matter where it starts.




<a name="FlightPlan">
## Search Probe Flight Plan</a>
The objective of the challenge is to survey an area in the shortest possible time.

ASSUMPTION: Targets are on the ground?

STRATEGY: The vehicle "probes" by incrementally first looking at the ground, then the walls, and finally the ceiling (for Spiderman).

STRATEGY: <strong>Fly high</strong> to best scan for targets

STRATEGY: To find targets, the vehicle "probes" by incrementally s

STRATEGY: Augment with assist from a central server?

<a name="ImageAcquisition">
## Image Acquistion</a>

Camera

Computing a 3D pose will require knowing the camera's focal length.

The homography is provided for applications that want the full 3D pose (position and orientation) of the tag in camera-relative coordinates:
hamming, goodness.

Conversion of tag coordinates to absolute positions requires <strong>calibration</strong> of the camera (iPhone).

<a name="TargetID">
## 3D Target Identification</a>
As a proxy for people and animals which are the ultimate target for the eventual objective after this challenge, AprilTags two-dimensional bar codes are used to compute 3D positions with respect to the camera.

<img alt="AprilTagsampler.png"  src="https://cloud.githubusercontent.com/assets/300046/13027844/927665ee-d21b-11e5-8a07-b79654ca3886.png">
The 6x6 monochrome bits on AprilTags encode small (between 4 and 12 bit) data payloads for robust detection from longer ranges (for high localization accuracy).
AprilTag outperforms ARToolkit in terms of detection rates and accuracy. 

587 values are in the 36h11 image set, currently the recommended one. 

QUESTION: What software will be used?

QUESTION: What customizations of the software will be needed?

STRATEGY _ : An arbiter master program chooses or merges outputs from several algorithms.
	Optical Flow (LK) is fast but unstable.
	SURF is accurate but slow.

<a target="_blank" href="https://april.eecs.umich.edu/wiki/index.php/AprilTags">
The iOS version of AprilTags</a> transmit tag detections via UDP port 7709 to another machine for additional processing. An example decoder (in Java) is available. http://robocomp.readthedocs.org/en/latest/code-examples/apritagstutorial/

SOFTWARE: https://april.eecs.umich.edu/wiki/index.php/AprilTags-C
is written in object-oriented style of GNU99 C.

https://en.wikipedia.org/wiki/Netpbm_format


 
<a name="RTH">
## Return To Home</a>
OBJECTIVE: Be able to back-track route without GPS
by remembering obstacles encountered and plotting a direct course around them back to origin.

<a name="Landing">
## Landing</a>
... on a moving target.

"Mission timer stops when the M100 motors switch off.” so ideally the drone would power itself off.


<a name="Research">
## Ref for research</a>
* https://april.eecs.umich.edu/pdfs/olson2011tags.pdf
* https://dspace.mit.edu/bitstream/handle/1721.1/83725/864440992-MIT.pdf?sequence=2
* http://www.engineering.com/DesignerEdge/DesignerEdgeArticles/ArticleID/11354/Drones-Dodge-Obstacles-in-Real-Time.aspx
* https://github.com/andybarry/flight



