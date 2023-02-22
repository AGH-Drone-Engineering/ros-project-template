FROM osrf/ros:melodic-desktop-full


ARG DEBIAN_FRONTEND=noninteractive
RUN apt-get update


# GUI
RUN apt-get install -y lxde --no-install-recommends
RUN apt-get install -y xvfb x11vnc
ENV FD_GEOM=1920x1080
ENV FD_SESS=lxde


# Utils
RUN apt-get install -y vim git curl wget


# source ROS at startup
RUN echo source /opt/ros/${ROS_DISTRO}/setup.bash >> /root/.bashrc


CMD ["x11vnc", "-create", "-forever"]
EXPOSE 5900
