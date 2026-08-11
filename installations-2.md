# Quick guide - worth a try

##### Check ubuntu version
    lsb_release -a
##### Update Ubuntu's package list
    sudo apt update

##### Install tools needed to add the ROS repository
    sudo apt install curl gnupg2

##### Download ROS's security key
    sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg

##### Add the ROS 2 package repository to Ubuntu
    echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(. /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null

##### Update Ubuntu's package list again, now including ROS 2
    sudo apt update

##### Install ROS 2 Lyrical Desktop
    sudo apt install ros-lyrical-desktop