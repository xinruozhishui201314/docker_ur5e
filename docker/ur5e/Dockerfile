FROM nvidia/opengl:1.1-glvnd-runtime-ubuntu18.04

RUN apt-get update && apt-get install -y --no-install-recommends curl lsb-release wget gnupg
RUN sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
RUN curl -sSL 'http://keyserver.ubuntu.com/pks/lookup?op=get&search=0xC1CF6E31E6BADE8868B172B4F42ED6FBAB17C654' | apt-key add -

RUN apt-get update && DEBIAN_FRONTEND="noninteractive" apt-get install -y --no-install-recommends tzdata
RUN apt-get update && apt-get install -y --no-install-recommends \
    ros-melodic-desktop-full \
    ros-melodic-gazebo-ros-pkgs \
    ros-melodic-gazebo-ros-control \
    ros-melodic-ros-control \
    ros-melodic-ros-controllers \
    ros-melodic-control-toolbox \
    ros-melodic-moveit \
    ros-melodic-effort-controllers \
    ros-melodic-forward-command-controller \
    ros-melodic-joint-state-controller \
    ros-melodic-joint-trajectory-controller \
    ros-melodic-position-controllers \
    ros-melodic-velocity-controllers \
    ros-melodic-tf \
    ros-melodic-tf2-tools \
    ros-melodic-robot-state-publisher \
    ros-melodic-genpy \
    ros-melodic-roslint \
    python-catkin-tools \
    byobu \
    libudev-dev \
    python-pip \
    git \
    vim \
    net-tools \
    build-essential
ADD bringup.bash /
RUN echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
RUN echo "source /catkin_ws/devel/setup.bash" >> ~/.bashrc
