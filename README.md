## 寒假作业 moveit2 相关功能包的调用

## 项目描述
这是一个用于控制机械臂的 ROS2-humble-MoveIt2的项目，主要用 Docker 和 ROS 2 构建。
（launch配置文件基于MoveIt Setup Assistant工具生成）
## 一.安装步骤

1. 克隆仓库：
    ```bash
    https://github.com/QizhengTian/moveit2.git
    ```

2. 构建容器：
    ```bash
    cd .devcontainer       #进入工作空间
    docker compose build   #创建容器
    docker compose up
    ```
    

3. 从另一个终端进入容器：
    ```bash
    docker exec -it moveit2-container bash
    ```

## 二.启动项目
1.创建节点
```bash
colcon build
source /opt/ros/humble/setup.bash
source /ros_ws/install/setup.bash
```
2.运行生成的launch文件
```
ros2 launch my_moveit2 launch.py
```

##注：
若想改变基础模型，可在moveit2/ros_ws/src/my_moveit2/urdf里改变panda.urdf.xacro文件（基础模型文件），并修改部分其余文件中相关位置
本作借鉴https://github.com/wyq123-star/moveit2.git

