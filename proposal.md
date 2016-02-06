
The strategy of this team is to minimize both:

   I. the risk of running into obstacles and

   II. the likelihood of identifying and reaching survivors with the minimum effort.

<hr />

Here are the specific stragies which drive the innovative design:

STRATEGY A: The drone's flight path is based on a <strong>prioritized list</strong> of possible targets 
and <strong>flight paths</strong>, 
which the drone flies to in order. 
The destination of highest likelihood (based on results of object recognition) is at the top of the list.

STRATEGY B: The drone operates <strong>autonomously</strong>, 
but can be aided by additional input from powerful machine-learning servers
that informs the drone about areas of heightened or reduced interest.
For example, the server can cross-correlate information about specific objects based on searches of databases on the internet.

(Operation of multiple drones at the same time is beyond the scope of this current challenge,
but it is one aspect why drones need to prioritize some areas over others.)

STRATEGY C: Pictures from the drone would <strong>go through the mobile phone</strong>
which receives and forwards media from the drone to the server, then notifies the drone with information from the server.

STRATEGY D: The location of obstacles identified by the drone but not also recognized by the server 
are transmitted back to the server to refine object recognition algorithms.

STRATEGY E: Images taken are saved on a server's database for comparison across time,
and to use for the basis of additional learning.

STRAGEGY F: On its way to a waypoint/destination, the drone takes pictures of what’s enroute, building a full catalog of the field.
Each image is time and geo-coded with elevation data.

STRATEGY G: The higher the resolution of the camera on the drone, the higher the drone can fly.
Upon takeoff, the drone <strong>first flies high</strong> over the middle of the field to be at a high vantage point for 
taking a hi-res overview picture used to identify objects and prioritize waypoints.
"Conventional" approaches (such as the CNN Google uses) are based on the 2-dimentional pictures.

This is recognizing there's an FAA enforced 400 foot ceiling as well as No Fly Zones (NFZs)
http://www.dji.com/fly-safe/category-mc?www=v1

STRATEGY H: <strong>Flying vertically</strong> up and down would avoid obstacles better that flying horizontally.

STRATEGY I: There is a chance that the server is slow in coming back with its recommendations.
In case that happens, the drone circles near the perimeter of its mission field 
to take <strong>pictures at different angles</strong> to obtain a better chance of detecting objects,
hoping that the better granularity closer to objects may improve image recognition.

STRATEGY J: Pictures are used by the server to construct a <strong>3D model</strong> of the terrain and obstacles.

STRATEGY K: Before each flight, the drone's altimeter and other sensors are calibrated to ensure accuracy
needed to better compare data across different days and drone units.

