## 1. source.md是我bashrc的备份
## 2. https://mirrors.ustc.edu.cn/help/ubuntu-releases.html
## 是各类镜像源
## 3. 函数就是接口
## 4. PID算法
### 原理
![PID公式](/home/xin/docs/picture/PID.jpg)
### 公式
![PID公式](/home/xin/docs/picture/PID公式.png)
### 理解
#### 1. 比例调节
##### u=kp*error
对于一个存在误差的系统，
## 5. 在每打开一个终端的时候，就会跑一遍bashrc
如果写了两行代码
source ~/catkin_ws/devel/setup.bash
source ~/rm_ws/devel/setup.bash
跑一遍后，source的是后来那个
## 6. 鱼香ros
```
https://fishros.org.cn/forum/topic/20/%E5%B0%8F%E9%B1%BC%E7%9A%84%E4%B8%80%E9%94%AE%E5%AE%89%E8%A3%85%E7%B3%BB%E5%88%97?lang=zh-CN
```
## 7. 开pr

- ###  (1. folk仓库

进入别人仓库点击folk

- ### (2. clone仓库

进入自己仓库页面，复制folk下来的仓库的ssh地址

```
git clone ssh地址
```

- ### (3. 在自己电脑终端修改clone下来的仓库

- ### (4. push修改后的文档

```
git add 内容
```
内容可用
```
git status
```
查看

```
git commit -m '注释'
```

```
git push
```
## 8. ecat灯
- ### 1. can左右两个蓝灯，闪着正常
- ### 2. 顺着can过去，一个蓝灯，一个橙灯，是5V和3.3V的nuc降压电源灯，3.3V是为stm32服务的
- ### 3. 最上面板子那个最大最亮的绿灯是从站，与我电脑的网口配对，正常情况下是常闪
- ### 4. 从站下面是板子短侧边缘是裁判端和dbus的串口，正常是常绿
