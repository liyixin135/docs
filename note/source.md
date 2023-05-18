# 团队建立了私有软件源，可以不用从本地电脑上传就可以获取安装rm_controls和rm_controllers
## 1.添加公钥
```
wget -O - https://rmsource.gdutelc.com/ubuntu/key/public.key | sudo apt-key add -
```
## 2.添加源
```
echo "deb https://rmsource.gdutelc.com/ubuntu/ focal main" | sudo tee -a /etc/apt/sources.list
```
## 3.更新软件源
```
sudo apt update
```
# 有时候更新不成功就直接进行第四步
## 4.查找可安装的最新版本的rm_controls以及rm_controllers
```
sudp apt search ros-noetic-rm
```
(tab补齐)

### 注意：安装源后，在rm_ws/src下并没有对应的功能包rm_controls和rm_controllers功能包，而是有了它们的软件源，即不能在路径下找到这些功能包，但能正常使用
