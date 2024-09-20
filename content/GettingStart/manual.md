+++
title = 'manual'
date = 2024-09-21T1:28:29+08:00
weight = 2
draft = false
+++

## 1. 配置Node.js 环境

拷贝`node-v16.20.2-linux-x64.tar.xz`

右键解压,将解压的文件夹放置在home下

打开终端,运行命令

```bash
echo 'export PATH=" ~/node-v16.20.2-linux-x64/bin:$PATH"' >> ~/.bashrc
```

## 2. 安装可视化软件

拷贝`rds_packed_pantograph.tar.xz`

右键解压,将解压的文件夹放置在home下

在`~/rds_packed_pantograph`路径下打开终端,运行命令

```bash
node build.js
```

提示运行成功即可

浏览器中输入

`localhost:3000`

若外部访问,输入软件部署所在主机IP

e.g. `192.168.3.4:3000`

## 3. 安装插件

在`~/rds_packed_pantograph`中找到`wzq.project_pantograph-1.0.0`文件,拖动至浏览器内安装成功

## 4. 导入布局文件

在`~/rds_packed_pantograph`中找到两个**json**文件

**robot_arm.json**

**sensor_data.json**

分别在两个页面导入, 点击右上角菜单,查看,通过文件导入布局,选择json文件

![image-20240921015040755](manual.assets/json.png)

## 5. 连接ROS

点击菜单，打开连接，选择Rosbridge，输入ROS主机的IP，点击Open

![image-20240921015455760](manual.assets/connection.png)

![image-20240921015541695](manual.assets/rosbridge.png)