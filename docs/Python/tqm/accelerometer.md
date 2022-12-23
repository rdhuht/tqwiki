# 三轴传感器 accelerometer

## 简介

主板中的三轴传感器，检测姿态和运动。

## 函数

### 姿态检测

#### get_state()

获取姿态。<br>
*参数*：无。<br>
*返回值*：`state_name` 字符串。姿态的名称。<br>

姿态有以下可能性：

| 返回值  | 说明  |
|:----:|:----:|
| `shake` | 摇晃 |
| `up` | 标志朝上  |
| `down` | 标志朝下  |
| `left` | 向左倾斜 |
| `right` | 向右倾斜 |
| `face up` | 屏幕朝上  |
| `face down` | 屏幕朝下  |

```py title="acc_state.py" linenums="1" hl_lines="6"
from tqm import accelerometer
import time, serial

while True:
    time.sleep_ms(200)
    s = accelerometer.get_state()
    serial.write(s)

```

### 获取三轴强度

#### get_x()

#### get_y()

#### get_z()

读取三轴的加速度数值。<br>
*参数*：无<br>
*返回值*：<br>
`value` 整数。x/y/z方向上的三轴加速度的强度数值。<br>
单位：million-g。 <br>
范围：+/- 2000mg(开发板向右倾斜、标志朝上和屏幕朝上时value数值是正数；相反的是负数)。<br>

```py title="acc_value.py" linenums="1" hl_lines="6"
from tqm import accelerometer
import time, serial

while True:
    time.sleep_ms(200)
    x = accelerometer.get_x()
    serial.write(x)
```
