# 计时器 timer

## 简介

主板内的计时器。

## 函数

### 重置计时器

#### reset()

计时器归零，重新计时。<br>

*参数*：无。<br>

*返回值*：无。<br>

### 获取运行时间

#### running_time()

获取计时器计时秒数<br>

*参数*：无。<br>

*返回值*：second(s), 整数。运行时间多少秒，秒数值。<br>

```py title="timer.py" linenums="1" hl_lines="4 6"
from tqm import timer, serial
import time

timer.reset()
time.sleep(1)
rt = timer.running_time()
serial.write_num(rt)
time.reset(1)
time.sleep(3)
rt2 = timer.running_time()
serial.write_num(rt2)


```
