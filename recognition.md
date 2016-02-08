This article describes now AprilTags are recognized by software.

In order to figure out the optimal camera altitude and magnification levels needed for reliable image recognition.

## Identify range of effectivity

For repeatability and comparability:
   * Use a string and weight from the camera to make positioning repeatable
   * Mark position and stength of light source to position the same way each time.
   * Measure light strengh with a hand-held light meter.

Effectiveness of image recognition is measured in percentage of 100. ???

Design and print fiducial markers of different sizes on a standard 8.5x11 paper
(AprilTags).
Take a picture of the target at different feet lengths away from the target.

   * https://april.eecs.umich.edu/wiki/index.php/AprilTags
   * https://itunes.apple.com/us/app/apriltag/id736108128?mt=8
   * Ed Olson's https://april.eecs.umich.edu/apriltags/ is no longer available.

TEST STRATEGY A: Obtain a baseline number at close range with maximum light and flat angle.

   * 400 feet is the maximum from FAA?

TEST STRATEGY B: Repeat the test using different <strong>light levels</strong>.
Numbers are in Lumens.

   * QUESTION: When would the drone need an additional light source?

TEST STRATEGY C: Position AprilTags at <strong>different angles</strong>.
0 degrees is flat to the camera. 45 is the incline.

   * If angles are an issue, the drone would need to fly around more.

TEST STRATEGY D: Try different telephoto <strong>lenses</strong>.
The standard lens is 3.7 mm = 20 mm in 35 mm terms. See video with one: https://www.youtube.com/watch?v=JViCoX57fFU


<a name="Results">
## Results</a>
Runs are planned to obtain numbers at the extremes, so we don't waste our time with experiments for intermediate values.

| Strategy | Lens | Light | Feet | Angle | Description | Effectiveness |
| -------- | ---- | ----: |----: | ----: | ----------- | ------------- |
|        A |  std |  5000 |   10 |     0 | Closest - baseline |  99 |
|        B |  std |   500 |  400 |     0 | Farthest Extreme low light | 15? |
|        C |  std |  5000 |   10 |    45 | Extreme angle | 15 |

NOTE: The above are sample values provided for illustrative purposes.

## Out of scope:

This information can be in the app to assist.

<a target="_blank" href="http://meshlab.sourceforge.net/">
MeshLab</a> to analyze 3D objects (unstructured 3D triangular meshes)
from an <a target="_blank" href="https://occipital.com/">Occipital</a> 3D sensor
and Bridge Engine for mixed reality.

http://freecode.com/projects/shadevis
to render shading (ambient occlusion).

