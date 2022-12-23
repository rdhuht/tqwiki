# WiFi

## 简介

网络。

## 函数

### 连接网络

#### connect(name, password)

连接网络。<br>

*参数*：<br>
`name` 字符串。热点的名称。<br>
`password` 字符串。热点的密码。<br>
*返回值*：无。

```py
from tqm import wifi

name = ""
password = ""
wifi.connect(name, passoword)

```

### 判断连接状态

#### is_connected()

判断连接是否成功。

*参数*：无。<br>
*返回值*：`value` 布尔值。True连接成功，False连接失败。

```py
from tqm import wifi

name = ""
password = ""
wifi.connect(name, passoword)
```

### 断开连接

#### disconnect()

断开连接。

*参数*：无。

*返回值*：无。

```py
from tqm import wifi

name = ""
password = ""
wifi.connect(name, passoword)
```
