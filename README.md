## 微信跳一跳辅助opencv实现
### 运行效果
<figure class="half">
<image src="https://github.com/csuhan/wechatJump/blob/master/img/1_41.png"  />
<image src="https://github.com/csuhan/wechatJump/blob/master/img/4_26500.png"/>
</figure>

### 基本思路
* adb截屏并上传到电脑
* 匹配棋子，从而得到棋子位置
* Canny边缘提取，搜索下一个格子面顶点
* 区域生长，搜索整个格子面
* 格子面中心点即为下一个位置
* 计算两点距离，乘以时间系数（1080p的系数为1.395左右）
* adb 模拟swipe
### 存在的问题
当然了作为一个业余项目，没有考虑那么多，对于色差较大的格子，有时候就会计算不准确。

接下来就等高分了，hhhh（虽然已经被微信封了，但是享受过程嘛）
