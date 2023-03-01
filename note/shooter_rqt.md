# 使用rqt实现发射

## 1.连接nuc

## 2.关闭自启
```
sudo systemctl stop rm_start.service start_master.service
```
注意，如果补齐不出来，就证明自启应该关闭了

## 3.运行roscore

## 4.打开硬件接口
```
mon launch rm_config rm_hw.launch
```

## 5.加载控制器
```
mon launch rm_config load_controllers.launch
```

## 6.rqt控制发射

点击plugin下的robot_tool下的controller_manager

start两个calibration校准，听声音，一个是拨盘校准，一个是云台校准

## 7.发布话题命令发射

点击plugin下的topics下的message publisher

选中话题:/controller/shooter_controller/command

1是stop
2是ready
3是push
先ready再push，urdf设置的拨盘offset才会生效
注意记得勾选

