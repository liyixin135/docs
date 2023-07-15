# can

## 1.初始化can
```
sudo ip link set can0 up type can bitrate 1000000
```
```
sudo ip link set can1 up type can bitrate 1000000
```

## 2.监听can上的数据
```
candump can0
```
```
candump can1
```
