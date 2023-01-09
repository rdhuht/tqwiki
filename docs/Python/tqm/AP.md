# 无线局域网热点 wlan

## 简介

本地不需要WiFi，就可以建立AP热点，进行数据发送等操作。

## 函数

### 创建局域网热点

#### creat_AP(name, password)

创建局域网热点。

*参数*：<br>
`name`，字符串。热点名称。<br>
`password`，字符串。热点密码。

*返回值*：无。

### 连接状态

#### wifi.is_connected()

判断热点是否连接成功。

*参数*：无<br>

*返回值*：<br>
`state` 布尔值。状态。True连接成功，False连接失败。

```py title="connectWifi.py" linenums="1" hl_lines="3 4"
from tqm import wifi

wifi.connect("ssid","password")
if wifi.is_connected():
  display.show_icon("happy")
else:
  display.show_icon("sad")
```

### 断开连接
#### wifi.disconnect()

断开无线热点的连接<br>
*参数*：无。<br>
*返回值*：无。
