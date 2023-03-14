# 关于自启

## 关自启
```
sudo systemctl stop rm_start.service start_master.service
```

## 开自启
```
sudo systemctl start rm_start.service start_master.service
```

- 注意：通电后打开机器人的nuc，机器人就会自启，此时可以用遥控器控制机器人，若要用自己电脑控制机器人，需要把自启关闭。没关闭就打开roscore就会出现以下报错：
RLException: ERROR: could not contact master [http://机器人ip]
The traceback for the RLException was written to the log file
[master] killing on exit
