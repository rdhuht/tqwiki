# 旋钮传感器 rotarySwitch

## 简介

旋钮传感器（又叫电位器），是用手控转的手动元件，信号的输出方式为模拟信号，可以将单圈旋转的角度转变为电压变化，测量范围0~300°。

<figure markdown>
  ![旋钮传感器返回值](../../img/旋钮传感器返回值.png){ width="400" loading=lazy}
  <figcaption>旋钮传感器返回值</figcaption>
</figure>

## 使用场景
<figure markdown>
  ![万用表](../../img/万用表.jpg){ width="400" loading=lazy}
  <figcaption>万用表</figcaption>
</figure>
<figure markdown>
  ![录音机](../../img/录音机.jpg){ width="400" loading=lazy}
  <figcaption>录音机</figcaption>
</figure>
<figure markdown>
  ![汽车空调开关](../../img/汽车空调开关.jpg){ width="400" loading=lazy}
  <figcaption>汽车空调开关</figcaption>
</figure>

## 函数

### 旋转值

#### get_value(port)

获得旋钮的旋转数值。<br>
*参数*：<br>
`port`，整数，端口。扩展板端口2到5分别对应端口P2到P5。</br>

*返回值*：<br>
`value`，整数。返回值的理想范围是0~1023。

!!! warning "注意"
    实际的返回值可能与0~1023的理想值范围有出入，可以使用map函数进行范围的映射变更。

```py title="rotarySwitch.py" linenums="1" hl_lines="1 9"
from tqe1 import rotarySwitch
from tqm import serial
import math

i = 0

while True:
  time.sleep_ms(200)
  i = rotarySwitch.get_value(2)
  serial.write_num(math.map(i, 5, 1014, 0, 100))

```
