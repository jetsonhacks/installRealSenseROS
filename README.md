# installRealSenseROS
Install the realsense-ros library on NVIDIA Jetson Developer Kits.
<br>MIT License
<br>Copyright (c) 2018-20 JetsonHacks

The installRealSenseROS script will install librealsense and realsense_camera as ROS packages. These scripts have been tested with a RealSense D435, D435i and T265 cameras.

Note that the RealSense ROS wrapper is for ROS Kinetic, but the Jetson L4T 31.X (Ubuntu 18.04) is ROS Melodic. Please note any issues that you encounter.

This is the third step of a three step process.

The first step requires the installation of librealsense (version 2). 

One way to accomplish this is to use the 'installRealSenseSDK' repository on the Github JetsonHacks account (https://github.com/jetsonhacks/installRealSenseSDK). There are also scripts to build the librealsense library itself <em><b>Note: </b>You will need to use the matching version of librealsense which corresponds to the RealSense ROS wrapper. See release notes below.</em>

The second step is to install ROS on the Jetson. There are convenience scripts to help do this on the Github JetsonHacks account in the installROS repository (https://github.com/JetsonHacks/installROS). Note that the repository installs ros-base, if other configurations such as ros-desktop are desired, the scripts can do that through the command line parameters. You may want to install rviz. <em><b>Note: </b>realsense-ros officially only supports ROS Kinetic presently, the Jetsons runs ROS Melodic. While we haven't run into any issues running the library under ROS Melodic, be aware that there may be differences</em>.

This repository, the third step, is to install realsense-ros. The script installRealSenseROS.sh in this directory will install realsense-ros and dependencies in a Catkin Workspace.

To install:

$ ./installRealSenseROS.sh \<catkin_ws_name\>

The script 'disableAutosuspend.sh' simply turns off the USB autosuspend setting on the Jetson so that the camera is always available. 


<h3>Releases:</h3>
<b>January 2020</b>

* Initial Release
* L4T 32.3.1
* JetPack 4.3
* Requires librealsense v2.31.0
* Installs RealSense ROS Version = 2.2.11

