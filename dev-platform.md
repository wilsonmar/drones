## Development Enviornment

This describes the development platform, packaged within a (large)
VMware Fusion 8 .vmwarevm bundle (WIN-HIJA4A33DRG) with 3.37 GB RAM running within a 2.49 GHz Mac OSX Yosemite.

NOTE: Fusion 8 places emphasis on graphics-intensive virtualization
(supporting DirectX 10 and OpenGL 3.3). See http://www.networkworld.com/article/3023246/virtualization/review-run-windows-10-on-your-mac-using-vmware-s-fusion-8.html

## Windows 7 Base Utilities

* Windows 7 Ultimate SP1
* Chocolatey
* Java 7.0.79.1 using cinst jdk7 from https://chocolatey.org/packages/jdk7
  (not jdk-7u79-windows-x64.exe from http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html)
* 7z938-x64.msi
* Git-1.9.5-preview20141217.exe

* android-studio-bundle-141.2456560-windows.exe from http://developer.android.com/sdk/installing/index.html?pkg=studio
* SourceTreeSetup_1.6.20.exe

<hr />

<a name="MobileSDK">
## Mobile SDK</a>
DJI's Mobile SDK at home page https://developer.dji.com/mobile-sdk/
consists of:

* Firmware for each DJI model (Phantom 3, Inspire 1, OSMO, 
* DJI PC Simulator Installer & User Manual
* WIN Driver Installer
* iOS SDK and SDK Sample and Release Notes
* Android SDK and SDK Sample and Release Notes for version 3.0.1 on Feb 4, 2016, update from 2.4)
 
http://developer.dji.com/mobile-sdk/documentation/
provides docs on classes, protocols, constants generated from code at
https://github.com/dji-sdk/Mobile-SDK-Android/tree/master/Sample%20Code

But more useful is https://developer.dji.com/en/get-started/mobile-sdk/Mobile-SDK-Features/

Contributors include https://github.com/JonasVautherin
who also contributed to https://github.com/3drobotics/solodevguide
and http://code.opencv.org/projects/opencv/wiki
doing http://code.opencv.org/projects/opencv/wiki/FaceDetection
Gary Bradski, President and CEO, OpenCV Foundation

### DJI PC Simulator Installer
Download from DJI's Mobile SDK at home page https://developer.dji.com/mobile-sdk/

DJISimulator-Installer.exe
requires DJI_WIN_Driver_Installer.exe installed into C:\Program Files (x86)\DJI Product\DJI driver2.02
and does not run on Windows 10 (only to Windows 8.1).

DJISimulator-Installer.exe within DJI_PC_Simulator_Installer_And_User_Manual_V1.0_en
into C:\Program Files (x86)\DJISimulator.

* https://developer.dji.com/en/get-started/mobile-sdk/Mobile-SDK-API-Introduction/
  contains color pictures of what is in DJI PC Simulator User Manual.pdf downloaded,
  except call-outs of flight data is transmitted to the PC through the UDP port 5566.
  The PC can interpret this data to create a virtual 3D environment for analysis.

<strong>WARNING: Use of Simulator requires the drone be connected to Windows via USB cable</strong>

### Open Android Studio
Since Android Studio doesn't install desktop icons by default:

0. Use Windows File Explorer to navigate to Androind Studio which installed to

   ```
   C:\Program Files\Android\Android Studio\bin
   ```

0. Invoke <strong>studio64.exe</strong>.

   Notice the program is now based on IntelliJ rather than Eclipse.

   WARNING: As of this writing, DJI documentation
   recommends using Eclipse and later convert to Studio.
   This tutorial takes it to the next step.

0. PROTIP: To open Android Studio quickly, right-click on the Desktop
   to create a new Shortcut to:

   ```
C:\Program Files\Android\Android Studio\bin\studio64.exe
   ```

   Name it "AndroidStudio" or whatever you like.


<a name="Decisions">
### Decide on Names</a>
These are harder and more time consuming than people think they should be.

   * App name: for example, "drone-android-app".
   * Project folder name and path. In a git repo folder? 
   * Company name.
   * Project location. Will a sub-domain be created?
   * Package name such as "com.dji.sdkdemo" in the example or "com.jetbloom.air-ranger".


### Read Reference Documentation
There are two places to read the docs for this:

* https://dji-dev.gitbooks.io/mobile-sdk-tutorials/content/en/Android/FPVDemo/FPVDemo_en.html
  seems to be older than:

* https://github.com/DJI-Mobile-SDK/Android-FPVDemo
  README.md


### Start New Android Project
Android Studio has a default location at the top of your User folder.

PROTIP: Use a folder for your project that is version controlled.

   https://github.com/wilsonmar/drone-android-app

0. Create in Github a new repo and clone it in a folder.
   As is customary with github, the folder would contain README.md
   and LICENSE.md files.

0. Open an internet browser and download a zip of the repo's master branch:

   https://github.com/DJI-Mobile-SDK/Android-FPVDemo

   NOTE: No need to clone it because we will not change it.

0. Unzip it.
0. Delete the images folder and README.md files because you can view them online.
0. Copy the FPV-Demo folder to your clipboard.
0. Using File Explorer, drill to the folder containing the sample app.
0. Copy the sample app source to your app's folder.
0. Within Android Studio, Start a New Android app based on the decisions above.
0. Provide the version-controlled file path created above.
0. PROTIP: If there is white space within a portion of the folder, find its 8-character equivalent:
   open a Command Window, navigate to the folder such as C:\Users. Use command:

   ```
   dir /X
   ```

   Copy the 8-character name, such as "WILSON~1" for "Wilson Mar".

0. In the Project location, replace the long name with the short name in your clipboard.
0. Click Next. (assumed in steps to follow)
0. Check Phone and Tablet. 
0. For Minimum SDK, select DJI-recommended <strong>API version 19: Android 4.4 (KitKat)</strong>.
0. Select "Add No Activity". Click Finish.

0. Specify a package name such as "com.dji.sdkdemo" in the example or "com.jetbloom.air-ranger".
0. Get the <strong>package</strong> from within the AndroidManifest.xml' file.
0. Go to File -> New -> Import Module. 
0. In the 'Source Directory' field, find the DJI-SDK-LIB folder location (Android Studio\DJI-SDK-Android-V2.1.0\Lib\DJI-SDK-LIB). 
0. Press Finish.
0. Press Alt+1 or View | Tool Windows | Project.
0. Expand your project by clicking the arrow to the left of your project name.

0. Run your app. 
0. Launch Emulator. The default "Nexus 5 API 23 x86".

   PROTIP: Select an Android virtual device that you also physically use.

0. Check Use same device for future launches.
0. Click the green arrow to initiate. If this message appears:

   [avd launch error haxm kern module not installed](https://cloud.githubusercontent.com/assets/300046/12910832/d6c6a940-cec2-11e5-94b6-dc6fad3ca4e1.png)

   (where HAXM = Hardware Accelerated eXecution Manager)

0. Go to https://software.intel.com/en-us/android/articles/intel-hardware-accelerated-execution-manager
0. Download haxm-windows_v6_0_1.zip (6.0.1) and unzip.
0. Invoke intelhaxm-android.exe.



   Android SDKs are stored in:

   ```
Windows: \Users\%USERNAME%\AppData\Local\Android\android-studio\sdk\
Mac: /Applications/Android\ Studio.app/sdk/
Linux: /usr/share/android-studio/data/sdk
   ```

### Get and Provide the API Key
0. Begin registration for Airmap at https://developer.dji.com/ by providing values from
   <a href="#Decisions">decision</a>.
0. Paste the key when creating the app at http://developer.dji.com/en/user/apps/#all
0. Open email from DJI with subject "Activate your app" and click the Activation link.
0. Click Save in the pop-up dialog. Click OK on the pop-up.
0. Copy the 24-digit hexadecimal App Key to your clipboard.

### Android app views
https://github.com/PhilJay/MPAndroidChart - A powerful Android chart view / graph view library, supporting line- bar- pie- radar- bubble- and candlestick charts as well as scaling, dragging and animations.
