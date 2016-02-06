
Since time is of the essence, a strategy is needed which minimizes:

  A. the risk of running into obstacles and

  B. the likelihood of finding survivors with the minimum effort.

STRATEGY 1: Flying vertically up and down would avoid obstacles better that across the field.

STRATEGY 2: The drone has a high resolution camera, so we want to leverage that.
Upon takeoff, the drone first flies high over the middle of the field to be at a high vantage point for 
taking a hi-res overview picture used to identify objects and prioritize waypoints.
"Conventional" approaches (such as the CNN Google uses) are based on the 2-dimentional pictures.

There's an FAA enforced 400 foot ceiling.

STRATEGY 3: The server issues a prioritized list of possible targets, which the drone flies to in order. 
The destination of highest likelihood is at the top of the list.

STRATEGY 4: Pictures from the drone would go through the mobile phone which receives and forwards media from the drone to the server.

STRATEGY 5: Images taken are saved on a server's database for comparison across time,
and to use for the basis of additional learning.

STRATEGY 6: There is a chance that the server is slow in coming back with a list.
In case that happens, the drone then circles the perimeter of its mission field 
to take pictures at different angles which provide a better chance of detecting objects,
hoping that the better granularity closer to objects may improve image recognition.

STRATEGY 7: The pictures are used by the server to construct a 3D model of the terrain and obstacles.

STRAGEGY 8: On its way, the drone takes pictures of what’s enroute, building a full catalog of the field.
Each image is geo coded.

STRATEGY 9: Before each flight, the drone's altimeter and other sensors are calibrated to ensure accuracy
needed to better compare data across different days and drone units.

Beyond the scope of this current set is operation of multiple drones at the same time.

