# Lidar
obstacle detection using scanse sweep

# Set-Up
### Download & Install the SDK
```bash
git clone https://github.com/scanse/sweep-sdk.git \
cd libsweep && \
mkdir -p build && \
cd build && \
cmake .. -DCMAKE_BUILD_TYPE=Release && \
cmake --build . && \
sudo cmake --build . --target install && \
sudo ldconfig
```

### Install the ROS Node
```bash
git clone https://github.com/scanse/sweep-ros.git
ln -s $(readlink -f sweep-ros) ~/catkin_ws/src
cm
refresh
```

### Configure the Port Permissions
```bash
chmod 777 /dev/ttyUSB0
```

### Run the Node:
```bash
roslaunch sweep_ros view_sweep_pc2.launch 
```
