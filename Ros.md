MarkDown安装
sudo apt-get install retext
retext Release-Notes.md

ROS的Indigo版本安装
1.配置Ubuntu仓库，Software&Updates中 Ubuntu Software下勾选"restricted," "universe," and "multiverse." 

2.安装源
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
或来自中国的源：
sudo sh -c '. /etc/lsb-release && echo "deb http://mirrors.ustc.edu.cn/ros/ubuntu/ $DISTRIB_CODENAME main" > /etc/apt/sources.list.d/ros-latest.list'

3.增加key
sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116
//sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 0xB01FA116

4.更新
sudo apt-get update

5.安装，这里介绍Desktop-Full安装: (Recommended) : ROS, rqt, rviz, robot-generic libraries, 2D/3D simulators, navigation and 2D/3D perception
sudo apt-get install ros-indigo-desktop-full

6.解决依赖
sudo rosdep init
rosdep update

7.环境设置
echo "source /opt/ros/indigo/setup.bash" >> ~/.bashrc
source ~/.bashrc

8.安装rosinstall,便利的工具
sudo apt-get install python-rosinstall

卸载Indigo
$ sudo apt-get remove ros-indigo-*  ///opt下的ROS文件夹indigo被删除

检查一下Linux的版本
lsb_release -a
检查ROS版本
roscore

Turtlebot入门
http://www.ncnynl.com/archives/201609/786.html

Turtlebot包安装
参考安装指南：http://wiki.ros.org/turtlebot/Tutorials/indigo/Turtlebot%20Installation
sudo apt-get update
sudo apt-get install ros-indigo-turtlebot ros-indigo-turtlebot-apps ros-indigo-turtlebot-interactions ros-indigo-turtlebot-simulator ros-indigo-kobuki-ftdi ros-indigo-rocon-remocon ros-indigo-rocon-qt-library ros-indigo-ar-track-alvar-msgs

