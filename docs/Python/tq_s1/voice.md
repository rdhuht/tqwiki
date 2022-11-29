# 声音传感器 voice
## 简介
获取声音强度。

## 函数
### 获取声音强度
#### get_intensity(port)
获取环境声音强度。</br>
*参数*：<br>
`port` 整数。端口，扩展板端口2到5分别对应端口P2到P5。</br>
*返回值*：<br>
`intensity` 整数。声音强度的数值，范围0～1023。

```py title="voice Intensity.py" linenums="1" hl_lines="3 9"
from tqm import serial
import time
from tqe1 import voice

port = 2

while True:
    time.sleep_ms(200)
    i = voice.get_intensity(port)
    serial.write_num(i)

```