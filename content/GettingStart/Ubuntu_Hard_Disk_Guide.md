+++
title = 'Ubuntu硬盘使用说明'
date = 2024-09-04T15:28:29+08:00
weight = 1
draft = true
+++


在机器人和无人机的开发过程中，Linux系统环境，配置总是最大的拦路虎，为了完成一个小实验或测试一个算法，可能需要搭建完整的仿真或实体实验环境，这不仅给新手带来了极大的难度，即便是经验丰富的开发者也会浪费大量宝贵时间。

为了解决这一难题，我们推出了一款特别设计的Ubuntu系统移动硬盘，专为机器人和无人机开发者及初学者提供便利。该移动硬盘不仅预装了常用的软件和系统环境，还搭建好了所有的仿真环境，以下是我们系统的主要特性：

## Linux系统

使用Ubuntu20系统进行配置。由于Ubuntu18系统版本较老，而且官方团队早已停止维护，并且在大多数新机器上会遇到驱动兼容性问题，以及软件适配性问题，故更将系统升级为Ubuntu20.04。

### 无人机仿真工具链

预装了PX4和ArduPilot的仿真工具链，支持多种无人机模型和飞控，确保全生态适用。用户只需按照手册操作，即可一键启动仿真环境，快速搭建自己的实验平台，无需繁琐配置。这不仅大大缩短了开发时间，还降低了配置错误的风险，让开发过程更加顺畅。

### 轮式机器人仿真环境

配置了完整的Gazebo仿真环境。用户可以根据手册进行自定义设置，替换不同的模型和ROS算法包，以实现预期效果。论是用于学习、教学，还是实际项目开发，用户都能轻松应对。此外，我们还提供了多种预配置的仿真场景，让用户可以快速开始实验。

### 实体遥控器接入无人机仿真

遥控器通过数据线连接电脑，可接入到我们配置好的仿真环境之中，使用实体遥控器操控仿真之中的无人机模型，更加方便的验证飞控功能，模拟不同的飞行场景。

### 硬件适配及即插即用

为了确保系统的兼容性和易用性，我们进行了大量优化，使其能够与指定的控制器模块即插即用。无论是传感器还是控制板，用户只需将硬件连接到移动硬盘，无需进行复杂的配置调整即可开始工作。这样的设计真正实现了开箱即用，极大地方便了开发者，节省了大量时间和精力。

### 网络和输入法优化

为提高系统的易用性，我们配置了Clash代理（提供免费节点），以应对各种网络状况，确保外网访问和资源下载顺畅。同时，预装了搜狗输入法，为用户提供更流畅的输入体验。

### 完善的开发环境

针对广大开发者，我们预装了gcc/g++和Python编译器，并配置了VScode、注册好的Pycharm。用户无需额外安装和配置，即可享受开箱即用的开发环境，大大提高开发效率。

### 大容量存储

我们的移动硬盘提供了256GB的高存储空间，其中128GB分配给Linux系统，另有128GB作为冗余空间。这部分空间既可作为Linux补充存储，也可单独作为移动硬盘存储资料文件，灵活应对不同的存储需求。

### 一键启动

为了方便用户使用多种软件和功能环境，我们在说明书中详细总结了各功能模块的启动代码，实现更加便捷的一键启动。用户无需记忆复杂的命令，轻松启动所需功能。

### 便携设计，兼容性强

这款Ubuntu系统移动硬盘不占用现有电脑硬盘空间，不影响现有电脑的Windows系统，随身携带，即插即用。无论是实验室还是外出调试，都能轻松携带和使用。

这款Ubuntu系统移动硬盘是机器人和无人机开发者的理想选择，不仅节省了宝贵时间，还提供了极大的便利性和灵活性。让开发者能够专注于创新和研发，推动技术进步。



## 移动硬盘使用说明

1. 如何进入硬盘 Ubuntu 系统
   - 将移动硬盘用数据线连接电脑 USB 口
   - 电脑启动时，按 DEL / F2 / F12 进入 BIOS 界面，找到 boot 选项
   - 选择移动硬盘 ubuntu(XDISK PSSD 0)作为第一引导


![image](/images/Ubuntu_Hard_Disk_Guide.assets/secure_boot.JPG)


> Tips:
>
> 1. 由于电脑主板品牌众多，进入 boot 选项方法有差异，具体可百度或则咨询电脑品牌商；
> 2. 在下次开机之前，先将移动硬盘插入电脑；开机后，会出现GRUB界面，可选择进入 Ubuntu 系统或是 Windows 系统。使用 Ubuntu系统时，移动硬盘不可拔出(拔出系统会崩溃)。而使用 Windows系统时，移动硬盘仍旧被当做外部存储设备，可随时弹出。
> 3. 若下次开机之前，未插入移动硬盘，且 BIOS 里面 boot 引导还是移动硬盘，这时电脑将无法显示任何界面，此时只能强制关机。将移动硬盘连接电脑后，重新开机进入 BIOS 界面，修改第一启动项为 PC 本机，才可正常使用 Windows 系统。

## Ubuntu系统登录

- 登录名：robot
- 密码：123
- 中英文切换快捷键（搜狗输入法）：win+空格


## 额外存储空间使用

磁盘名称为 **My Disk** , 拥有123GB的存储空间，可存储任意文件，与系统盘独立使用，不影响系统盘。




## Ardupilot 环境使用

### 源码项目路径

`~/Workspaces/ardupilot`

![image](/images/Ubuntu_Hard_Disk_Guide.assets/ardupilot_souce_code_file.png)

使用VScode打开源码

在侧边栏找到图标

点击打开VScode，右上角 `文件`菜单，点击 `打开文件夹`，选择 `~/Workspaces/ardupilot`

![image](/images/Ubuntu_Hard_Disk_Guide.assets/vscode.png)

### Ubuntu 系统下源码的编译和下载

```sh
#切换路径
cd ~/Workspaces/ardupilot

# 1. 查看支持的飞控板类型
./waf list_boards

# 2. 配置飞控板类型  
# 常用板子pixhawk2.4.8，编译时选择 fmuv3 的板
./waf --configure --board fmuv3

# 3. 将源码编译成固件 根据需求选择命令
./waf copter			#多旋翼
./waf copter 			#heli直升机
./waf rover				#车
./waf plane				#固定翼
./waf sub				#潜水器
./waf antennatracker	#追踪天线

#编译好的固件文件存放路径
~/Workspaces/ardupilot/build/fmuv3/bin

# 4.将固件上传到飞控 （上传前先将飞控用数据线连接电脑）
# 也可以直接用地面站软件，加载自定义固件，将固件上传至飞控
./waf --targets bin/arducopter --upload			#多旋翼
./waf --targets bin/arducopter-heli --upload	#直升机
./waf --targets bin/ardurover --upload			#车
./waf --targets bin/arduplane --upload			#固定翼
./waf --targets bin/ardusub --upload			#潜水器
./waf --targets bin/antennatracker --upload		#追踪天线

#若需要删除fmuv3/bin下编译好的固件
./waf clean
```

### SITL 仿真运行

```sh
cd ~/Workspaces/ardupilot/ArduCopter

sim_vehicle.py --console --map
```

![image](/images/Ubuntu_Hard_Disk_Guide.assets/SITL_run.png)

### Gazebo 仿真运行

终端1

```sh
gazebo --verbose worlds/iris_arducopter_runway.world
```

终端2

```sh
cd ~/Workspaces/ardupilot/ArduCopter

../Tools/autotest/sim_vehicle.py -f gazebo-iris --console --map
```

![image](/images/Ubuntu_Hard_Disk_Guide.assets/ardupilot_gazebo_SITl.png)

## PX4环境使用

### 源码项目路径

`~/Workspaces/PX4-Autopilot`

使用 VScode 浏览代码

### Ubuntu 系统下源码的编译和下载

```sh
# 切换目录
cd ~/Workspaces/PX4-Autopilot

# 编译固件
# 常用板子pixhawk2.4.8，编译时使用 fmuv3 的板
 make px4_fmu-v3_default

# 将固件编译并上传到飞控 （上传前先将飞控用数据线连接电脑）
make px4_fmu-v3_default upload
##########################################
Erase  : [====================] 100.0%
Program: [====================] 100.0%
Verify : [====================] 100.0%
Rebooting.

[100%] Built target upload

# 查看其他支持的飞控板
make list_config_targets
```

### SITL & Gazebo 联合仿真

```sh
# 切换目录
cd ~/Workspaces/PX4-Autopilot
# 启动SITL & gazebo
make px4_sitl gazebo-classic_iris
```

可以选择下列不同的飞行器仿真模型：

| Vehicle                                                      | Command                                                   |
| ------------------------------------------------------------ | --------------------------------------------------------- |
| [Quadrotor](https://docs.px4.io/main/en/sim_gazebo_classic/vehicles.html#quadrotor-default) | `make px4_sitl gazebo-classic`                            |
| [Quadrotor with Optical Flow](https://docs.px4.io/main/en/sim_gazebo_classic/vehicles.html#quadrotor-with-optical-flow) | `make px4_sitl gazebo-classic_iris_opt_flow`              |
| [Quadrotor with Depth Camera](https://docs.px4.io/main/en/sim_gazebo_classic/vehicles.html#quadrotor-with-depth-camera)(forward-facing) | `make px4_sitl gazebo-classic_iris_depth_camera`          |
| [Quadrotor with Depth Camera](https://docs.px4.io/main/en/sim_gazebo_classic/vehicles.html#quadrotor-with-depth-camera)(downward-facing) | `make px4_sitl gazebo-classic_iris_downward_depth_camera` |
| [3DR Solo (Quadrotor)](https://docs.px4.io/main/en/sim_gazebo_classic/vehicles.html#3dr-solo-quadrotor) | `make px4_sitl gazebo-classic_solo`                       |
| [Typhoon H480 (Hexrotor)](https://docs.px4.io/main/en/sim_gazebo_classic/vehicles.html#typhoon-h480-hexrotor)(with video streaming) | `make px4_sitl gazebo-classic_typhoon_h480`               |
| [Standard Plane](https://docs.px4.io/main/en/sim_gazebo_classic/vehicles.html#standard-plane) | `make px4_sitl gazebo-classic_plane`                      |
| [Standard Plane (with catapult launch)](https://docs.px4.io/main/en/sim_gazebo_classic/vehicles.html#standard-plane-with-catapult-launch) | `make px4_sitl gazebo-classic_plane_catapult`             |
| [Standard VTOL](https://docs.px4.io/main/en/sim_gazebo_classic/vehicles.html#standard-vtol) | `make px4_sitl gazebo-classic_standard_vtol`              |
| [Tailsitter VTOL](https://docs.px4.io/main/en/sim_gazebo_classic/vehicles.html#tailsitter-vtol) | `make px4_sitl gazebo-classic_tailsitter`                 |
| [Ackerman UGV (Rover)](https://docs.px4.io/main/en/sim_gazebo_classic/vehicles.html#ackermann-ugv) | `make px4_sitl gazebo-classic_rover`                      |
| [Differential UGV (Rover)](https://docs.px4.io/main/en/sim_gazebo_classic/vehicles.html#differential-ugv) | `make px4_sitl gazebo-classic_r1_rover`                   |
| [HippoCampus TUHH (UUV: Unmanned Underwater Vehicle)](https://docs.px4.io/main/en/sim_gazebo_classic/vehicles.html#unmanned-underwater-vehicle-uuv-submarine) | `make px4_sitl gazebo-classic_uuv_hippocampus`            |
| [Boat (USV: Unmanned Surface Vehicle)](https://docs.px4.io/main/en/sim_gazebo_classic/vehicles.html#hippocampus-tuhh-uuv) | `make px4_sitl gazebo-classic_boat`                       |
| [Cloudship (Airship)](https://docs.px4.io/main/en/sim_gazebo_classic/vehicles.html#airship) | `make px4_sitl gazebo-classic_cloudship`                  |

启动Gazebo 和 SITL 仿真

![image](/images/Ubuntu_Hard_Disk_Guide.assets/px4_gazebo_SITL.png)



### 完整启动ROS + MAVROS + gazebo + SITL

```sh
cd ~/Workspaces/PX4-Autopilot
DONT_RUN=1 make px4_sitl_default gazebo-classic
source Tools/simulation/gazebo-classic/setup_gazebo.bash $(pwd) $(pwd)/build/px4_sitl_default
export ROS_PACKAGE_PATH=$ROS_PACKAGE_PATH:$(pwd)
export ROS_PACKAGE_PATH=$ROS_PACKAGE_PATH:$(pwd)/Tools/simulation/gazebo-classic/sitl_gazebo-classic
#启动
roslaunch px4 posix_sitl.launch

#检查SITL飞控与MAVROS连接，connected: True 说明连接正常
rostopic echo /mavros/state
```

![image](/images/Ubuntu_Hard_Disk_Guide.assets/px4_ros_gazebo_SITL.png)


更多Gazebo Classic仿真资料可以查看[官方文档](https://docs.px4.io/main/zh/sim_gazebo_classic/)



## 地面站启动

### MissionPlanner地面站的启动

```sh
cd ~/MissionPlanner
mono MissionPlanner.exe
```

![image](/images/Ubuntu_Hard_Disk_Guide.assets/missionplanner.png)

### QGC 地面站的启动

```sh
cd ~
./QGroundControl.AppImage
```

![image](/images/Ubuntu_Hard_Disk_Guide.assets/qgc.png)

## 轮式机器人仿真

仿真源码路径：

`~/robot_ws`

启动终端：

```sh
# 设置环境变量
source ~/robot_ws/devel/setup.bash
#启动仿真
roslaunch neo_simulation simulation.launch
```

![image](/images/Ubuntu_Hard_Disk_Guide.assets/wheel_robot.png)



## 遥控器接入仿真操控无人机

启动ROS + MAVROS + gazebo + SITL 联合仿真：

终端1

```sh
#切换路径
cd ~/Workspaces/PX4-Autopilot
#设置环境变量
DONT_RUN=1 make px4_sitl_default gazebo-classic
source Tools/simulation/gazebo-classic/setup_gazebo.bash $(pwd) $(pwd)/build/px4_sitl_default
export ROS_PACKAGE_PATH=$ROS_PACKAGE_PATH:$(pwd)
export ROS_PACKAGE_PATH=$ROS_PACKAGE_PATH:$(pwd)/Tools/simulation/gazebo-classic/sitl_gazebo-classic
#启动
roslaunch px4 posix_sitl.launch
```

启动QGroundControl地面站

```sh
cd ~
./QGroundControl.AppImage
```

插入遥控器，点击地面站右上角图标，进入“Vehicle Setup”

![image](/images/Ubuntu_Hard_Disk_Guide.assets/controller_sim_1.png)

点击游戏手柄

![image](/images/Ubuntu_Hard_Disk_Guide.assets/controller_sim_2.png)


先进行遥控器校准，按照提示拨动摇杆每个方向

![image](/images/Ubuntu_Hard_Disk_Guide.assets/controller_sim_3.png)


再进行按钮分配，设置可以解锁（Arm）的拨杆

![image](/images/Ubuntu_Hard_Disk_Guide.assets/controller_sim_4.png)

![image](/images/Ubuntu_Hard_Disk_Guide.assets/controller_sim_5.png)


完成设置！

当地面站右上角显示“**Ready To Fly**” 意味着可以解锁正常飞行，只需拨动刚才设置的解锁（Arm）拨杆即可

![image](/images/Ubuntu_Hard_Disk_Guide.assets/controller_sim_6.png)

拨动右上角显示 “**Armed**”，轻推油门即可起飞！

![image](/images/Ubuntu_Hard_Disk_Guide.assets/controller_sim_7.png)

## Terminator 终端工具启动

使用快捷键：Ctrl+Alt+T，即可打开。鼠标右键点击终端窗口可设置垂直分屏或则水平分屏。

![image](/images/Ubuntu_Hard_Disk_Guide.assets/terminator1.png)

![image](/images/Ubuntu_Hard_Disk_Guide.assets/terminator2.png)

## 微信、向日葵远程桌面的启动

点击左下角 9 个点 **显示应用程序**，找到对应的图标点击打开应用程序。

![image](/images/Ubuntu_Hard_Disk_Guide.assets/wechat_icon.png)


![image](/images/Ubuntu_Hard_Disk_Guide.assets/wechat.png)


![image](/images/Ubuntu_Hard_Disk_Guide.assets/sun.png)