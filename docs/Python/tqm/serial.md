# 串口 serial

## 简介

使用串行接口与设备通信。

## 函数

### 串口设置

#### set_baud_rate(value)

设置波特率<br>
*参数*：<br>
`value`，整数。默认的数值是9600或者115200。

*返回值*：无。

```py title="serialbaudrate.py" linenums="1" hl_lines="3"
from tqm import serial

serial.set_baud_rate(115200)  # 设置波特率(1)
```

1. 默认的波特率是115200，如过没有特殊情况，可以不使用此函数

### 串口写入

#### serial.write_str(text)
#### serial.write_num(number)
#### serial.write_bool(boolean)

向串行端口写入一个字符串、数字、布尔值。

*参数*：<br>
`text`、`number`、`boolean`，字符串、数字、布尔值。要向串口写入的数据。

*返回值*：无。

```py title="write.py" linenums="1" hl_lines="3"
from tqm import serial

serial.write_str("I love China!")
serial.write_num(123)
serial.write_num(3.1415926)
serial.write_bool(True)
serial.write_bool(False)
```
