# Hikrobot_Vision_MultiCam_ROS
基于ROS的多个hikrobot usb摄像头启动程序

## 使用方法
本项目支持根据摄像头名称检索摄像头图像，并发布对应rostopic

### 配置环境
根据 https://blog.csdn.net/weixin_60003973/article/details/135824902 配置相机驱动，确保基于ROS的单摄像头程序能够运行，依次从终端获取对应摄像头名称<br>
例如:

    [device 0]:
    1
    [device 1]:
    2

此处摄像头名称分别为1、2
### 修改配置文件
根据摄像头名称修改/config/xxx.yaml文件中Camera_id <br>
例如：/config/camera_multicam_0.yaml <br>

    Camera_id: '0' 
    rostopic_name: '/hikrobot_camera_near/rgb'

此处摄像头名称分别为0, 图像topic为 /hikrobot_camera_near/rgb
### 启动
直接启动：

    roslaunch hikrobot_camera_multicam hikrobot_camera_multicam.launch

rviz启动：

    roslaunch hikrobot_camera_multicam hikrobot_camera_multicam_rviz.launch

### 添加摄像头
1. 编写yaml文件
2. 修改launch文件

## 参考资料 & 特别鸣谢
教程：
https://blog.csdn.net/weixin_60003973/article/details/135824902

单相机ros驱动:
https://gitcode.com/luckyluckydadada/HIKROBOT-MVS-CAMERA-ROS/overview?utm_source=csdn_github_accelerator&isLogin=1

hikrobot相机SDK文档：
https://vision.scutbot.cn/HikRobot/index.html


