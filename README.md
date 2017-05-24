# Lidar
Getting Scanse Sweep to work using ROS

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
# Without visualization:
roslaunch sweep_ros sweep.launch
# or with visualization:
roslaunch sweep_ros view_sweep_pc2.launch 

```
