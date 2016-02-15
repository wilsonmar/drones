# SAP Use of Drones

A drone can be used for <strong>visual inspection of physical goods</strong>
such as shipping containers and automobiles sitting on a shipyard.

In some ways, a drone can be a safer and faster option than people climbing on ladders, especially where potentially toxic air can be present (such as at an oil refinery).

For example, a drone can fly on a designated flight path through the factory
taking a video. The video are fed into a Machine Learning algorithm to detect bar codes. 

Bar codes on items would be used to positively identify each item. Special Machine visual Learning algorithms would glean numbers from within pictures.

Codes found are verified against the location in the system and the location is updated if inconsistencies are found. The location of objects that cannot be identified automatically are sent to human inspectors.

Alternately, the precise 3D location of items are entered within the SAP Materials Management module. A system then calculates a flight path among them, taking pictures. 

Additionally, pictures are compared over time and an alert is sent if differences or other anomalies are found.

Large physical goods are handled by several SAP modules:

   * ![Plant Maintenance = PM](http://www.erpgreat.com/sap-pm.htm)
   * Materials Management (MM)
   * Quality Management (QM)

Websites providing more information about these SAP modules include:

   * http://erpgreat.com/

QUESTION: Are DJI drones free of sparks?

This new system would require a new database holding images and videos captured from drones and maintain metadata about each image, such as:

   * URL to the picture/video file within a media database
   * Location of item within the Warehouse Management system
   * Location of item pictured
   * Location of drone when it took the picture
   * Time media was taken (if within a video, the time-stamp in the video)
   * Values extracted from bar codes in the picture
   * Link to a report of defects observed on item
