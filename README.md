# Ubuntu20.04 + ROS Noetic 安装记录

## 一、安装步骤
1. VMware虚拟机安装Ubuntu 20.04操作系统，完成系统初始化，切换国内清华镜像软件源，提升下载速度。
2. 按照ROS‑Noetic官方文档，配置软件源、导入密钥，执行apt命令完整安装ros‑noetic‑desktop‑full。
3. 在~/.bashrc中配置ROS环境变量，source生效，验证ROS版本。
4. 测试turtlesim小乌龟示例，分别运行roscore、turtlesim_node、teleop_key，实现键盘控制海龟移动。

## 二、遇到的问题与解决方案
1. apt下载速度很慢：更换清华大学Ubuntu软件源。
2. ROS密钥校验失败：重新导入GPG密钥，使用国内ROS镜像源。
3. 小乌龟方向键不动：必须点击聚焦键盘控制的终端窗口，再按方向键。
4. source之后ROS命令找不到：没有把环境变量写入.bashrc，每次打开终端要source。

## 三、验证结果
- Ubuntu版本：20.04
- ROS版本：Noetic
- turtlesim仿真可以正常键盘控制运动
