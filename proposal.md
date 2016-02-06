
The strategy of this team is to minimize both:

   A). the risk of running into obstacles and

   B). the likelihood of identifying and reaching survivors with the minimum effort.

Here are the specific stragies which drive the innovative design:

STRATEGY 1: Flying vertically up and down would avoid obstacles better that across the field.

STRATEGY 2: The drone's flight path is based on a prioritized list of possible targets and <strong>flight paths</strong>, 
which the drone flies to in order. 
The destination of highest likelihood is at the top of the list.

STRATEGY 3: The drone operates <strong>autonomously</strong>, 
but can be aided by additional input from powerful machine-learning servers
that informs the drone about areas of heightened or reduced interest.
For example, the server can cross-correlate information about specific objects based on searches of databases on the internet.

(Operation of multiple drones at the same time is beyond the scope of this current challenge,
but it is one aspect why drones need to prioritize some areas over others.)

STRATEGY 4: Pictures from the drone would go through the mobile phone which receives and forwards media from the drone to the server.

The location of obstacles identified by the drone but not recognized are transmitted back to the server to refine object recognition algorithms.

STRATEGY 5: The higher the resolution of the camera on the drone, the higher the drone can fly.
Upon takeoff, the drone first flies high over the middle of the field to be at a high vantage point for 
taking a hi-res overview picture used to identify objects and prioritize waypoints.
"Conventional" approaches (such as the CNN Google uses) are based on the 2-dimentional pictures.

This is recognizing there's an FAA enforced 400 foot ceiling.

STRATEGY 6: Images taken are saved on a server's database for comparison across time,
and to use for the basis of additional learning.

STRATEGY 7: There is a chance that the server is slow in coming back with a list.
In case that happens, the drone then circles the perimeter of its mission field 
to take pictures at different angles which provide a better chance of detecting objects,
hoping that the better granularity closer to objects may improve image recognition.

STRATEGY 8: The pictures are used by the server to construct a <strong>3D model<strong> of the terrain and obstacles.

STRAGEGY 9: On its way, the drone takes pictures of what’s enroute, building a full catalog of the field.
Each image is geo coded.

STRATEGY 10: Before each flight, the drone's altimeter and other sensors are calibrated to ensure accuracy
needed to better compare data across different days and drone units.

