# 串口 serial

## 简介

使用串行接口与设备通信。

## 函数

### 串口设置

#### set_baud_rate(value)

设置波特率
参数：num 整数 9600 或者115200 

*返回值*：无。

```py title="serialbaudrate.py" linenums="1" hl_lines="3"
from tqm import serial

serial.set_baud_rate(115200)  # 设置波特率(1)
```

1. 默认的波特率是115200，如过没有特殊情况，可以不使用此函数

### 串口写入

#### serial.write(value)

向串行端口写入一个数字。

*参数*：<br>
`value` int/float 整数/浮点数。要向串口写入的数值。

*返回值*：无。

```py
from tqm import serial

serial.write_num(123)
serial.write_num(3.1314)
```
