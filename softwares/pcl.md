# PCL installation

This is the installation of pcl-1.7
```bash
sudo add-apt-repository ppa:v-launchpad-jochen-sprickerhof-de/pcl
sudo apt-get update
sudo apt-get install libpcl-all
# if you cannot find libpcl-all, try following instead:
sudo apt-get install libpcl-dev
```
or you can visit: [pcl download](http://www.pointclouds.org/downloads/linux.html), [pcl official site](http://www.pointclouds.org/)

There are other ways to install pcl-1.8 but I failed to install it.

# Compiling PCL from source

The following instructions is for compiling PCL. The apporaches failed to install PCL on my machine so I had no choice but to compile it myself.

1. dependencies:
```bash
sudo apt-get update
sudo apt-get install git build-essential linux-libc-dev
sudo apt-get install cmake cmake-gui
sudo apt-get install libusb-1.0-0-dev libusb-dev libudev-dev
sudo apt-get install mpi-default-dev openmpi-bin openmpi-common
sudo apt-get install libflann1.8 libflann-dev
sudo apt-get install libeigen3-dev
sudo apt-get install libboost-all-dev
sudo apt-get install libvtk5.10-qt4 libvtk5.10 libvtk5-dev
sudo apt-get install libqhull* libgtest-dev
sudo apt-get install freeglut3-dev pkg-config
sudo apt-get install libxmu-dev libxi-dev
sudo apt-get install mono-complete
sudo apt-get install qt-sdk openjdk-8-jdk openjdk-8-jre
```

2. download and compile
```bash
git clone https://github.com/PointCloudLibrary/pcl.git  
cd pcl
mkdir release
cd release
cmake -DCMAKE_BUILD_TYPE=None -DCMAKE_INSTALL_PREFIX=/usr -DBUILD_GPU=ON -DBUILD_apps=ON -DBUILD_examples=ON -DCMAKE_INSTALL_PREFIX=/usr ..
make -j4 (线程数根据情况选择)
sudo make  install
```

3. use it with cmake
follow http://pointclouds.org/documentation/tutorials/using_pcl_pcl_config.php#using-pcl-pcl-config

