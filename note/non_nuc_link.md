# 使用can协议用自己电脑测发射

## 1.连接好can和电机后，打开电池，短按一下，长按一下，开通电源

## 2.初始化can

看清连接的是can0还是can1，对应初始化
```
sudo ip link set can0 up type can bitrate 1000000
```
```
sudo ip link set can1 up type can bitrate 1000000
```

## 3.监听can上的数据
```
candump can0
```
```
candump can1
```

## 4.改对应ip

-
根据读取的ip，例如206，点开rm_config下的CMakeLists,修改rm_hw下的hero.yaml中的tigger_joint_motor的id，例如0x206.

## 5.打开launch文件

```
roscore
```
```
mon launch rm_config rm_hw.launch
```
```
mon launch rm_congfig load_controllers.launch
```

## 6.使用rqt或者manual控制
