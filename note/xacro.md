# .xacro使用
### 拓展：xacro其实是urdf的升级版，urdf能实现的，xacro都能做到，但urdf做不到xacro能做到的宏定义、文件包含、条件判断等等的功能。
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

## 3.
①
```
<?xml version="1.0"?>
```
### 这段代码是XML文档的开头，包含了文档的版本信息和编码格式

### 拓展：XML是一种标记语言，用于存储和传输数据

## 4.定义
 ①<xacro:property name="wheel_radius" value="0.07625">
类似于C语言的宏定义 define

 ②<xacro:macro name="func" params="v1 v2">
  <!-- 代码块 -->
  </xacro:macro>
类似于void func(int v1,int v2);

## 5.调用
 ①<link name="${wheel_radius}"

 ②<xacro:func v1="" v2=""/>

## 6.引入文件
 <xacro:include filename="$(find mbot_description)/urdf/xacro/sensors/myrobot.xacro" />      <!--这个是引入文件的语法，find后面跟的是功能包-->

    <base_car/>
