# WiFi

## 简介

网络。

## 函数

### 连接网络

#### connect(name, password)

连接网络。
参数：

name 字符串，热点名称。

password 字符串，热点密码。

返回值：无。

```py
from tqm import wifi

name = ""
password = ""
wifi.connect(name, passoword)

```

### 判断连接状态

#### is_connected()

判断连接是否成功。

参数：无。

返回值：Bollean，布尔值。True连接成功，False连接失败。

```py
from tqm import wifi

name = ""
password = ""
wifi.connect(name, passoword)
```

### 断开连接

#### disconnect()

断开连接。

参数：无。

返回值：无。

```py
from tqm import wifi

name = ""
password = ""
wifi.connect(name, passoword)
```
