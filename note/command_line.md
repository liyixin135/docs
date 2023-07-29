# 命令行合集

## 1.  查看磁盘分区
```
df -h
```
## 2.  查看网口
```
ifconfig
```
或者
```
ip a
```
## 3.  不接交换机，网线连接
```
nmap 10.42.0.1/24
```
## 4.  部署交换机网口
```
# This is the network config written by 'subiquity'
network:
  ethernets:
    enp89s0:
      dhcp4: false
      optional: true
      addresses: [192.168.100.2/24]
      optional: true
      nameservers:
         addresses: [255.255.255.0]
  version: 2
```
若只是配个可以接网线的口，先进行第2点查看有什么网口，再部署
```
enp2s0：
   dhcp：true
   optionnal：true
```
## 5.  查看自启服务的状态
```
sudo systemctl status +服务名
```
## 6.  设置ROS_IP
```
export ROS_IP=网址IP
```
## 7.  开控时拨动速度摇杆，判断是否发送速度指令
```
rostopic echo /cmd_vel
```
## 8.  nuc/派勤进入网络管理界面
```
sudo python3 easywifi.py
```
## 9.  拉取多个源的仓库代码
```
git remote add 分支包名字 ssh地址
```
```
git fetch 分支包名字
```
例如
```
git remote add cgl ssh地址
```
```
git fetch cgl
```
## 10. 给其他ip设备发送压缩包
```
scp 路径+压缩包名称 用户名@IP
```
例
```
xin@xin:~/Downloads$ scp ~/Downloads/sysbench-1.0.20.tar.gz dynamicx@192.168.1.122:~/
```
回车后
sysbench-1.0.20.tar.gz                        100% 1474KB   2.3MB/s   00:00
拓展：
命令行中开头 用户名@计算机名
## 11. 获取其他ip设备的压缩包
```
scp 用户名+IP:路径+压缩包名称
```
## 12. 解压/打包.tar
解压
```
tar xvf xxx.tar
```
打包
```
tar cvf xxx.tar DirName
```
## 13. 解压/打包.tar.gz/.tgz
解压
```
tar zxvf FileName.tar.gz
```
打包
```
tar zcvf FileName.tar.gz DirName
```
## 14.  ssh免密登录
```
ssh-copy-id dynamicx@ip
```
## 15.  自启
1.  关闭自启
```
sudo systemctl stop rm_start.service start_master.service
```
若是没关闭自启打开roscore，则会出现以下报错:
 RLException: ERROR: could not contact master [http://机器人ip] The traceback for the RLException was written to the log file [master] killing on exit
2.  开自启
```
sudo systemctl start rm_start.service start_master.service
```
3.  关闭加开启
```
sudo systemctl restart rm_start.service start_master.service
```
