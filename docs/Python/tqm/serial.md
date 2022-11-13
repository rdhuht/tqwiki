# 串口

## 简介

Communicate with a device using a serial interface

## 函数

### 串口设置

#### serial.set_baud_rate(value)

设置波特率
参数：num 整数 9600 或者115200 

返回值：无。

```py
from tqm import serial
```

### 串口写入

#### serial.write(value)

Write a buffer to the bus..

参数：value  A bytes object or a string.

返回值：The number of bytes written, or `None` on timeout。

```py
from tqm import serial

serial.write('hello world')
serial.write(b'hello world')
serial.write(bytes([1, 2, 3]))
```
