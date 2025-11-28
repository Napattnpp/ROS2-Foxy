Jetson Nano and Docker



git clone https://github.com/dusty-nv/jetson-containers
cd jetson-containers
./install.sh



sudo docker run --runtime nvidia -it --rm \
    --network host \
    --device /dev/ttyACM0 \
    --device /dev/ttyUSB0 \
    --volume ~/my_robot_code:/root/ros2_ws/src \
    dustynv/ros:humble-ros-base-l4t-r32.7.1



