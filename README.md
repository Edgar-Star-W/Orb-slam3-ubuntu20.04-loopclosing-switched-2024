

# 1. Intro
ORB-Slam3 has been tested by its creator on ubuntu 16 and 18, as time goes, some dependencies have been decapitated and codes need to be modified. This is a guide for you to successfully install and run ORB-Slam3 in 2024 on Ubuntu 20.04. The code has been modified so that the loop closure can be enabled/disabled by changing the parameter in the .yaml files in the Example directory. The implementation of loop-closure-switch was guided by https://github.com/hobbeshunter/ORB_SLAM3/commit/b7f00c3d9d6bb4c4f8c1cd4954375126b7927210

The author referred to https://github.com/aryaman-patel/orb_slam3_implementation for the solving some dependency problems

# 2. Installation 

1. Clone the this directory to your work space and rename it as ORB_Slam3

2. Install the following dependencies:

  sudo add-apt-repository "deb http://security.ubuntu.com/ubuntu xenial-security main"
  sudo apt update

  sudo apt-get install build-essential
  sudo apt-get install cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev

  sudo apt-get install python-dev python-numpy libtbb2 libtbb-dev libjpeg-dev libpng-dev libtiff-dev libdc1394-22-dev libjasper-dev

  sudo apt-get install libglew-dev libboost-all-dev libssl-dev

  sudo apt install libeigen3-dev


3. Install OpenCV
   OpenCV 4.4 must be installed.
   1. Download OpenCV 4.4 from the OpenCV website.
   2. cd to the downloaded OpenCV directory
   3. mkdir build
   4. cd build
   5. cmake -D CMAKE_BUILD_TYPE=Release -D WITH_CUDA=OFF -D CMAKE_INSTALL_PREFIX=/usr/local ..
   6. make -j 3
   7. sudo make install
4. Install Pangolin:
   Follow the instruction here: https://github.com/stevenlovegrove/Pangolin (it was tested without with Ninja)
   Note ./scripts/install_prerequisites.sh recommended might raise some problem, ./scripts/install_prerequisites.sh required can be a good alternative
5. Download ORB-Slam3 from here (with loop-closure-switching) or https://github.com/UZ-SLAMLab/ORB_SLAM3.git which is standard
   cd to ORB-Slam3 directory
   run ./build.sh

Testing procedures can be found here: https://github.com/aryaman-patel/orb_slam3_implementation for the solving some dependency problems
   







