# Installing-opencv
# Installing opencv in raspberry pi 
# You need to open terminal and copy each commands.

################################
# Method-1

# Open up the terminal and paste the commands:
sudo apt install python3-opencv

# If this method doesn't works then follow the method-2

# Method-2

# Step-1
# Update Raspbian to the latest version:
sudo apt-get update && sudo apt-get upgrade && sudo rpi-update

# Step-2
# Increase the swap-size:
sudo nano /etc/dphys-swapfile
# After running this command you will see "CONF_SWAPSIZE=100". Comment it by adding "#" and add " CONF_SWAPSIZE=2048" and press ctrl + O

# Step-3
# Install tools and libraries for openCV:
sudo apt-get install build-essential cmake pkg-config

sudo apt-get install libjpeg-dev libtiff5-dev libjasper-dev libpng12-dev

sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev

sudo apt-get install libxvidcore-dev libx264-dev

sudo apt-get install libgtk2.0-dev libgtk-3-dev

sudo apt-get install libatlas-base-dev gfortran
# Copy each command and paste it to the terminal and repeat this for another. If there you see asking for yes/no type "y"

# Step -4
# You need to download and unzip as follows:
wget -O opencv.zip https://github.com/opencv/opencv/archive/4.1.0.zip

wget -O opencv_contrib.zip https://github.com/opencv/opencv_contrib/archive/4.1.0.zip

unzip opencv.zip

unzip opencv_contrib.zip

# Step-5
# Install numpy:
sudo pip3 install numpy

# Step-6
# Build OpenCV:
# It will takes much time nearly to 3-4 hours be calm.
make -j4

# Step-7
# Installing opencv:
sudo make install && sudo ldconfig

# Step-8
# Reboot your system:
sudo reboot

# Step-9
# Now opencv is installed in your pi. You can check it by running following in terminal:
python3

import cv2

# cv2.__version__

