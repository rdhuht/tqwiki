# 计时器 timer

## 简介

主板内置的计时器。

## 函数

### 重置计时器

#### reset()

计时器归零。<br>

*参数*：无。<br>

*返回值*：无。<br>

### 获取运行时间

#### running_time()

获取运行秒数（主板通电后、重启后或调用reset函数后）。<br>

*参数*：无。<br>

*返回值*：`second(s)` 整数。运行时间多少秒，秒数值。<br>

```py title="timer.py" linenums="1" hl_lines="5 7 9"
from tqm import timer, serial
import time

time.sleep(1)
rt = timer.running_time()
serial.write_num(rt)
time.reset()
time.sleep(3)
rt2 = timer.running_time()
serial.write_num(rt2)

```
