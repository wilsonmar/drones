# Navigation 
This page describes the strategies core to the Challenge.

<a href="#Takeoff">Take-off</a> > <a href="#FlightPlan">Search Route</a> > <a href="#ImageAcquisition">Image Acquisition</a> -> <a href="#TargetID">Target Identification</a> > <a href="#RTH">Return</a> > <a href="#Landing">Landing</a>

QUESTION: Are these the stages?


<a name="Pre-Flight">
## Pre-Flight</a>

Before take-off, there is a built-in automatic check for no-fly zone
described in the References section.

<a name="Takeoff">
## Take-off</a>
![drone-on-truck](https://cloud.githubusercontent.com/assets/300046/12867256/81a776a0-cc9d-11e5-9a44-43f086b546c1.png)
Photo from <a target="_blank" href="https://www.youtube.com/watch?v=_kXoUsqzzMU">
video Introducing the SDK Challenge</a>


QUESTION: How is the home base for the drone delimited?

STRATEGY: <strong>Fast take-off</strong> to avoid air disturbance of the support vehicle and to maximize time.

The vehicle knows which direction to begin based on coordinates keyed in prior to takeoff.

The landscape is akin to a maze. There will be some dead-ends requiring back-tracking.

QUESTION: A basic pattern of flight needs to be selected.

STRATEGY a: <strong>Start from center then circle out?</strong>

STRATEGY b: <strong>Start from a corner?</strong>

STRATEGY c: <strong>Random?</strong> Maybe it doesn't matter where it starts.




<a name="FlightPlan">
## Search Probe Flight Routing</a>
The objective of the challenge is for the drone to <strong>autonmously survey</strong> an area in the shortest possible time.

The arena is 50x50 meter arena = 164x164 square feet

![drone dji developer challenge arena](https://cloud.githubusercontent.com/assets/300046/12867343/d4bb8442-cc9f-11e5-8b78-720c7e0cf464.jpg)
Photo from <a target="_blank" href="https://www.youtube.com/watch?v=_kXoUsqzzMU">
video Introducing the SDK Challenge</a>

SIDE NOTE: How high is 164 feet? Watch a high dive: https://www.youtube.com/watch?v=rEiwAAHakI0

QUESTION: How is the 50 x 50m delimited? With GPS coordinates but also recognizable visible physical boundaries too?


ASSUMPTION: Targets are on the ground?

STRATEGY: <strong>Fly high</strong> to best scan for targets

STRATEGY: To find targets, the vehicle "probes" by incrementally s

STRATEGY: Augment with assist from a central server?

QUESTION: For the challenge, are we limited to the example scenario in the rules doc? What type of terrain should the search and rescue be involved in/limited to? e.g. If we restrict the drones in no-fly zones, is it not permitted for search and rescue in those areas?

The M100 has an on-board <strong>collision avoidance</strong> capability.

STRATEGY: The vehicle "probes" by incrementally first looking at the ground, then the walls, and finally the ceiling (for Spiderman).




SOFTWARE for maze-solving.


<a name="ImageAcquisition">
## Image Acquistion</a>

Video from the Matrice M100 is taken from a Zenmuse X3 camera attached to a $2,499 Sony RX100 Gimbal (steadicam)

   * http://www.chasingame.com/moultrie-m100-camera-review/
   * http://www.dronenerds.com/products/matrice/sony-rx100-gimbal-for-dji-matrice-100-and-dji-inspire-1-rx100gimbal-dronenerds.html

The camera has thermo-imaging capabilities in the infra-red spectral range:
![p-gps spectral](https://cloud.githubusercontent.com/assets/300046/13034276/64d0b22e-d2ee-11e5-93b5-a25dbfffd516.png)


TODO: Computing a 3D pose requires knowing the camera's <strong>focal length</strong>.

The homography is provided for applications that want the full 3D pose (position and orientation) of the tag in camera-relative coordinates:
hamming, goodness.

CHECKLIST: Conversion of tag coordinates to absolute positions requires <strong>calibration</strong> of the camera (iPhone).

<a name="TargetID">
## 3D Target Identification</a>
![apriltag localization boxes](https://cloud.githubusercontent.com/assets/300046/13028142/72274224-d223-11e5-89f9-de86b8b15deb.png)

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

QUESTION: What software will be used to recognize images?
SOFTWARE: Options include:
* https://april.eecs.umich.edu/wiki/index.php/AprilTags-C
   is written in object-oriented style of GNU99 C.
* Microsoft Oxford
* Google Tensorflow

https://en.wikipedia.org/wiki/Netpbm_format


 
<a name="RTH">
## Return To Home</a>
OBJECTIVE: <strong>Back-track route</strong>. Be able to back-track route without GPS
by remembering obstacles encountered and plotting a direct course around them back to origin.

<a name="Landing">
## Landing</a>
... on a moving target.

"Mission timer stops when the M100 motors switch off.” so ideally the drone would power itself off as soon as it lands. 

STRATEGY: A "POWER OFF" button on the consoler?


<a name="Research">
## Ref for research</a>
* https://april.eecs.umich.edu/pdfs/olson2011tags.pdf
* https://dspace.mit.edu/bitstream/handle/1721.1/83725/864440992-MIT.pdf?sequence=2
* http://www.engineering.com/DesignerEdge/DesignerEdgeArticles/ArticleID/11354/Drones-Dodge-Obstacles-in-Real-Time.aspx
* https://github.com/andybarry/flight



