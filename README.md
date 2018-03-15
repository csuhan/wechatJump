## 微信跳一跳辅助opencv实现

> 79行代码实现简易微信跳一跳辅助，经测试可以达到5000+分数

> 本程序在opencv3.3环境下运行，其他版本未测试，请务必配置opencv
> 请在跳一跳程序运行时再运行本程序

### 运行结果

| ![](https://github.com/csuhan/wechatJump/blob/master/img/1_41.png) | ![](https://github.com/csuhan/wechatJump/blob/master/img/4_26500.png) |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| ![](https://github.com/csuhan/wechatJump/blob/master/img/39_17035.png) | ![](https://github.com/csuhan/wechatJump/blob/master/img/50_6868.png) |



### 基本思路
> 安卓调试工具adb可以对设备截图并上传至电脑
1. adb截屏并上传到电脑

2. 匹配棋子，从而得到棋子位置

3. Canny边缘提取，搜索下一个格子面顶点

4. 区域生长，搜索整个格子面

5. 格子面中心点即为下一个位置

6. 计算两点距离，乘以时间系数（1080p的系数为1.395左右）

7. adb 模拟swipe

### 文件说明
```c++
wechatJump.cpp : 主程序
player.png :棋子图片
jump.png : 实时手机截图
img : 部分匹配结果
```

### 存在的问题

当然了作为一个业余项目，没有考虑那么多，对于色差较大的格子，有时候就会计算不准确。

接下来就等高分了，hhhh（虽然已经被微信封了，但是享受过程嘛）