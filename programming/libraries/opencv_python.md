# OpenCV v3 for Python

## About

[OpenCV](http://docs.opencv.org/2.4/doc/tutorials/introduction/linux_install/linux_install.html) - OpenCV for Image Processing in Python 2.7.11+.

## Installing Dependencies

Install the dependencies for OpenCV:
```
sudo apt-get install build-essential
sudo apt-get install python-numpy python-scipy python-matplotlib
sudo apt-get install cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev
sudo apt-get install python-dev python-numpy libtbb2 libtbb-dev libjpeg-dev libpng-dev libtiff-dev libjasper-dev libdc1394-22-dev
```

## Downloading OpenCV

Launch Git client and clone [OpenCV repository](http://github.com/itseez/opencv). Or, via terminal:
```
cd ~/<working _directory>
git clone https://github.com/Itseez/opencv.git
```

## Installing OpenCV

Put the generated Makefiles in a temporary directory:
```
cd ~/opencv
mkdir release
cd release
cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local ..
```

Install OpenCV:
```
make
sudo make install
```
