# dense-flow
```shell=
sudo apt-get upgrade
sudo apt-get install build-essential cmake unzip pkg-config
sudo apt-get install libjpeg-dev libpng-dev libtiff-dev
sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev
sudo apt-get install libxvidcore-dev libx264-dev
sudo apt-get install libgtk-3-dev
sudo apt-get install libatlas-base-dev gfortran
sudo apt-get install python-dev
sudo wget -O opencv.zip https://github.com/opencv/opencv/archive/3.4.4.zip
sudo unzip opencv.zip
sudo mv opencv-3.4.4 opencv
sudo wget -O opencv_contrib.zip https://github.com/opencv/opencv_contrib/archive/3.4.4.zip
sudo unzip opencv_contrib.zip
sudo mv opencv_contrib-3.4.4 opencv_contrib
cd ~/opencv
sudo mkdir build
cd build
sudo cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local/opencv/ -D WITH_CUDA=ON -D INSTALL_PYTHON_EXAMPLES=ON -D OPENCV_EXTRA_MODULES_PATH=~/opencv_contrib/modules -D BUILD_EXAMPLES=ON -D WITH_FFMPEG=ON -D CUDA_ARCH_BIN=6.0 -DBUILD_opencv_cudacodec=OFF ..
sudo make -j4
sudo make install
```
