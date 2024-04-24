# Library-Raspberry-Pi4
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install python3
sudo apt-get install build-essential python3-dev
sudo python3 setup.py install

#Grove seeed
curl -sL https://github.com/Seeed-Studio/grove.py/raw/master/install.sh | sudo bash -s -
sudo pip3 install seeed-python-dht

#DHT Adafruit
cd /
sudo apt-get update
sudo apt-get install build-essential python3-dev
sudo git clone https://github.com/adafruit/Adafruit_Python_DHT.git
cd Adafruit_Python_DHT
sudo python3 setup.py install

#MQTT
sudo pip3 install paho-mqtt

sudo pip3 install fastapi[all]
sudo pip3 install uvicorn
sudo pip3 install pymongo





sudo apt-get install -y libopenblas-base libopenmpi-dev
sudo apt install -y libjpeg-dev zlib1g-dev

wget https://developer.download.nvidia.com/compute/redist/jp/v50/pytorch/torch-1.12.0a0+2c916ef.nv22.3-cp38-cp38-linux_aarch64.whl
sudo pip3 install torch-1.12.0a0+2c916ef.nv22.3-cp38-cp38-linux_aarch64.whl

wget -O opencv.zip https://github.com/opencv/opencv/archive/4.5.1.zip
wget -O opencv_contrib.zip https://github.com/opencv/opencv_contrib/archive/4.5.1.zip
unzip opencv.zip
unzip opencv_contrib.zip

mv opencv-4.5.1 opencv
mv opencv_contrib-4.5.1 opencv_contrib
rm opencv.zip
rm opencv_contrib.zip

cd ~/opencv
mkdir build
cd build

cmake -D CMAKE_BUILD_TYPE=RELEASE \
-D CMAKE_INSTALL_PREFIX=/usr \
-D OPENCV_EXTRA_MODULES_PATH=~/opencv_contrib/modules \
-D EIGEN_INCLUDE_PATH=/usr/include/eigen3 \
-D WITH_OPENCL=OFF \
-D WITH_CUDA=ON \
-D CUDA_ARCH_BIN=5.3 \
-D CUDA_ARCH_PTX="" \
-D WITH_CUDNN=ON \
-D WITH_CUBLAS=ON \
-D ENABLE_FAST_MATH=ON \
-D CUDA_FAST_MATH=ON \
-D OPENCV_DNN_CUDA=ON \
-D ENABLE_NEON=ON \
-D WITH_QT=OFF \
-D WITH_OPENMP=ON \
-D WITH_OPENGL=ON \
-D BUILD_TIFF=ON \
-D WITH_TBB=ON \
-D BUILD_TBB=ON \
-D BUILD_TESTS=OFF \
-D WITH_EIGEN=ON \
-D WITH_V4L=ON \
-D WITH_LIBV4L=ON \
-D OPENCV_ENABLE_NONFREE=ON \
-D INSTALL_C_EXAMPLES=OFF \
-D INSTALL_PYTHON_EXAMPLES=OFF \
-D BUILD_NEW_PYTHON_SUPPORT=ON \
-D BUILD_opencv_python3=TRUE \
-D OPENCV_GENERATE_PKGCONFIG=ON \
-D BUILD_EXAMPLES=OFF ..

make -j4

sudo make install

sudo rm -rf ~/opencv
sudo rm -rf ~/opencv_contrib

cd ~
sudo -H pip3 install -U jetson-stats

sudo reboot

python3













#Supervisor
sudo apt-get install supervisor
