# 计时器

## 简介

主板内的计时器。

## 函数

### 重置计时器

#### timer.reset()

设置波特率
参数：无。

返回值：无。

```py
from tqm import timer
```

### 获取运行时间

#### timer.running_time()

获取计时器计时秒数

参数：无。

返回值：ms 毫秒数值。

```py
from tqm import timer, serial
import time

timer.reset()
time.sleep(1)
rt = timer.running_time()
serial.write(rt)

```
