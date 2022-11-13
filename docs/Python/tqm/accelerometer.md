# 三轴传感器

## 简介

主板中的三轴传感器，检测姿态和运动。

## 函数

### 姿态检测

#### accelerometer.get_state()

获取姿态。
参数：无。
返回值：String 字符串。

姿态有以下可能性“shake”"up""down""left""right""face up""face down"。

```py
from tqm import accelerometer
import time, serial


while True:
    time.sleep_ms(200)
    s = accelerometer.get_state()
    serial.write(s)

```

### 获取三轴强度

#### accelerometer.get_x()

#### accelerometer.get_y()

#### accelerometer.get_z()

读取三轴的强度。
参数：无
返回值：int 整数。

```py
from tqm import accelerometer
import time, serial


while True:
    time.sleep_ms(200)
    x = accelerometer.get_x()
    serial.write(x)
```
