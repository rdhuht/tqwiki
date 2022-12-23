# 时间 time

## 简介

测量时间并给程序添加延迟。
## 函数

### 延时

#### time.sleep(s)

延迟几秒钟。<br>
*参数*：<br>
`s` 整数。延迟的秒数，second(s)秒。<br>
*返回值*：无。

```py title="delays.py" linenums="1" hl_lines="5 7"
from tqm import display
import time

while True:
  time.sleep(1)
  display.show_icon("heart")
  time.sleep(1)
  display.show_icon("hollow heart")
```

#### time.sleep_ms(ms)

延迟给定的毫秒数。<br>
*参数*：<br>
`ms` 整数。延迟的毫秒数，million second(s)毫秒。<br>

*返回值*：无。

```py title="delayms.py" linenums="1" hl_lines="5 7"
from tqm import display
import time

while True:
  time.sleep_ms(500)
  display.show_icon("heart")
  time.sleep_ms(500)
  display.show_icon("hollow heart")
```
