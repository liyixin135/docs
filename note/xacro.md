# .xacro使用
### xacro其实是urdf的升级版，urdf能实现的，xacro都能做到，但urdf做不到xacro能做到的宏定义、文件包含、条件判断等等的功能。
## 1..xacro不能直接使用，要转成.urdf
### 使用xacro生成urdf时，根标签robot中必须包含命名空间声明xmlns:xacro = "http://www.ros.org/wiki/xacro"
```
<robot name = "hero" xmlns:xacro="http://www.ros.org/wiki/xacro">
</robot>
```
颠倒顺序无异
```
<robot xmlns:xacro="http://www.ros.org/wiki/xacro" name="hero">
</robot>
```
## 2..urdf作用
### urdf是机器人的描述文件，gazebo中加载的仿真机器人是根据urdf加载的
### 发布tf的时候也要通过urdf来得到坐标系名称、位置以及不同坐标系之间的关系
