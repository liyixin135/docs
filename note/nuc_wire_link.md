# 网线连接机器人

## 1.插上网线

## 2.连接ip地址
点击右上角的网线图标，点击Wired Connected下的Wired Settings,点击Wired项的设置图标，从Details读取本机的ip地址，点击IPv4，点击Shared to other computers,最后点击Apply

## 3.使用nmap命令
```
nmap 10.42.0.1/24
```
读取机器人的ip

## 4.使用ssh协议连接上机器人
```
ssh dynamicx@ip
```
