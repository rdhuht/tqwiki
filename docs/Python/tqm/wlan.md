# 网络 wifi

## 简介

主板连接无线网络。

??? note "注意"
    天启主板目前的Wi-Fi支持2.4GHz频段，支持IEEE802.11b/g/n。

??? tip "WLAN与Wi-Fi的关系"
    无线局域网WLAN（Wireless Local Area Network）是一种无线计算机网络，使用无线信道代替有线传输介质连接两个或多个设备形成一个局域网LAN（Local Area Network），典型部署场景如家庭、学校、校园或企业办公楼等。WLAN是一个网络系统，而我们常见的Wi-Fi是这个网络系统中的一种技术。所以，WLAN和Wi-Fi之间是包含关系，WLAN包含了Wi-Fi。

## 函数

### 连接网络

#### wifi.connect(ssid, password)

连接无线热点。

*参数*：<br>
`ssid`，字符串。无线网络热点的名称。<br>
`password`，字符串。无线网络热点的密码。

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
