# 点阵屏

## 简介

全彩灯模块可以亮起不同颜色的灯光。
采用WS2812，是一个集控制电路与发光电路于一体的智能外控LED光源。
全彩灯模块可以实现多种颜色的显示。

## 函数

### 控制全彩灯颜色

#### RGB.set_color(port, color, brightness)

设置全彩灯的颜色和亮度</br>
参数：
</br>port，整数 扩展板端口 P1---P5
</br>color，元组 (r, g, b) 每个颜色是整数，范围是0~255
</br>brightness，整数 亮度范围0~100

返回值：无。

```py
import tqm
from tqe1 import RGB

port = 5
color = (100, 120, 0)
brightness = 90

RGB.set_color(port, color, brightness)

```
