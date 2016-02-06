

## DJI GO Android app
0. Install the app on one of your Android smart phones: 
   https://play.google.com/store/apps/details?id=dji.pilot&hl=en

   It works with the ZENMUSE X5R gimbal on the Inspire 1, Phantom 3 and Matrice 100 flying platforms 
   
   It also collects media from the Osmo handheld gimbal and camera.

   * control the camera
   * collects media 
   * edit videos
   * share media to the SkyPixel aerial photography community.
   * Detailed flight records.
   
   WARNING: There are complaints by users who complain about the app draining battery,
   especially after an app update.

0. Alternately, install the iPhone app from:
   https://github.com/dji-sdk/Mobile-SDK-iOS

## Use template dji-sdk/Mobile-SDK-Android

0. Create an App and get the API key.
0. Install Android Studio 1.5 from 
   http://developer.android.com/sdk/index.html.
0. Create a project folder.
0. git clone https://github.com/dji-sdk/Mobile-SDK-Android
0. Paste the API key in the AndroidManifest.xml.
0. Set the minimum SDK version as API 19.
0. File -> New -> Import Module. Find the DJI-SDK-LIB folder location. Press Finish.
0. In Dependencies, Choose Module :DJI-SDK-LIB.
0. Build and run project.
0. Update the firmware 


## Use DJI-Mobile-SDK/Android-FPVDemo
Write code to show video from the drone's camera:

0. clone tutorial at
   https://github.com/DJI-Mobile-SDK/Android-FPVDemo
   created by oliverou.
0. DJISDKManager

The end result is this:

   <img alt="recordvideo" src="https://cloud.githubusercontent.com/assets/300046/12869989/819ea920-cce4-11e5-9986-4000b346402e.png">

## UI Guidelines:
0. Use large transparent buttons like other DJI apps (DJI-Mobile-SDK/Android-FPVDemo):

0. Position touchable buttons matching locations as in the Ford SYNC dashboard view.
0. Use generic button shapes for international audences. ???
0. Toggle buttons with color (red for recording, clear for ready to record).

   * Clear Capture button turns to red and "Stop recording" when pressed.
     This would eliminate a button.
   * Play/Pause.

0. Other screens (tabs):

   * Missions list
   * Map of mission
   * List of waypoints (flight path) for mission selected, such as current mission.
   * List of media transferred to server (listed by time).
   * Data from server
   