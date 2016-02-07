This article describes now AprilTags are recognized by software.

In order to figure out the optimal altitude to 

## Identify range of effectivity

For repeatability and comparability:
   * Use a string and weight from the camera to make positioning repeatable
   * Mark position and stength of light source to position the same way each time.
   * Measure light strengh with a hand-held light meter.

Effectiveness of image recognition is measured in percentage of 100. ???

TEST STRATEGY A: Design AprilTags of different sizes on a 8.5x11 page.
Take a picture of the target at different feet lengths away from the target.

TEST STRATEGY B: Repeat the test using different <strong>light levels</strong>.
Numbers are in Lumens.

TEST STRATEGY C: Position AprilTags at <strong>different angles</strong>.
0 degrees is flat to the camera.

TEST STRATEGY D: Try different <strong>telephoto lenses</strong>.
The standard lens is 3.7 mm = 20 mm in 35 mm terms. See video with one: https://www.youtube.com/watch?v=JViCoX57fFU


<a name="Results">
## Results</a>
Runs are planned to obtain numbers at extremes, so we don't waste our time.

| Strategy | Light | Feet | Angle | Description | Effectiveness |
| -------- |-----: |----: | ----: | ----------- | ------------- |
| A | 5000 |   10 |   0 | Closest - baseline |  99 |
| B |  500 | 1000 |   0 | Low light | 15 |
| A | 5000 | 1000 |   0 | Farthest | 15 |


## Out of scope:

<a target="_blank" href="http://meshlab.sourceforge.net/">
MeshLab</a> to analyze 3D objects (unstructured 3D triangular meshes)
from an <a target="_blank" href="https://occipital.com/">Occipital</a> 3D sensor
and Bridge Engine for mixed reality.

http://freecode.com/projects/shadevis
to render shading (ambient occlusion).

