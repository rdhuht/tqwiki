# 蜂鸣器 buzzer

## 简介

蜂鸣器，根据输入的频率不同，产生不同的声音。可以用它做安全警报，也可以播放“蜂鸣器音乐”。<br>
工作原理是利用电磁感应现象，音频信号电流通过电磁线圈，使电磁线圈产生磁场，震动膜片在电磁线圈和磁铁的相互作用下，震动发声。

<figure markdown>
  ![无源蜂鸣器](../../../img/buzzer.png){ width="400"}
  <figcaption>无源蜂鸣器</figcaption>
</figure>

## 使用场景

<figure markdown>
  ![打印机](../../img/打印机.jpeg){ width="400" loading=lazy}
  <figcaption>打印机提示音</figcaption>
</figure>
<figure markdown>
  ![烟雾报警](../../img/烟雾报警.jpg){ width="400" loading=lazy}
  <figcaption>烟雾报警声</figcaption>
</figure>
<figure markdown>
  ![定时器](../../img/定时器.jpg){ width="400" loading=lazy}
  <figcaption>定时器</figcaption>
</figure>

## 函数

### 播放音乐

#### play_music(port, num)

播放内置音乐。<br>
*参数*：<br>
`port` 整数，端口。扩展板端口0, 1, 2, 3分别对应端口P0、P1、P2、P3。<br>
`num` 整数，编号。编号和音乐的对应关系如下表：

| 编号  | 歌曲名  |
|:---:|:----:|
| `1` | 生日快乐 |
| `2` | 欢乐颂  |
| `3` | 葫芦娃  |
| `4` | 两只老虎 |
| `5` | 警鸣声  |

*返回值*：无。

```py title="buzzerMusic.py" linenums="1" hl_lines="2 6"
import tqm
from tqe1 import buzzer

port = 0
num = 1
buzzer.play_music(port, num)
```

### 播放音符 （开发中……）

#### play_tone(port, tone, duration)

控制蜂鸣器播放指定音调。

*参数*：  
`port` 整数，端口。扩展板端口0, 1, 2, 3分别对应端口P0、P1、P2、P3。  
`tone` 字符串，音调。音调对应关系如下表：

|  编号  |  八度  |  音名  |  唱名  |  频率(赫兹)  |
|:---:|:---:|:---:|:---:|:---:|
|  `0`   |  4  |  C          |  do  |  261.63  |
|  `1`   |  4  |  C^#^/D^b^  |  di  |  277.18  |
|  `2`   |  4  |  D          |  re  |  293.66  |
|  `3`   |  4  |  D^#^/E^b^  |  ri  |  311.13  |
|  `4`   |  4  |  E          |  mi  |  329.63  |
|  `5`   |  4  |  F          |  fa  |  349.23  |
|  `6`   |  4  |  F^#^/G^b^  |  fi  |  369.99  |
|  `7`   |  4  |  G          |  so  |  392.00  |
|  `8`   |  4  |  G^#^/A^b^  |  si  |  415.30  |
|  `9`  |  4  |  A          |  la  |  440.00  |
|  `10`  |  4  |  A^#^/B^b^  |  li  |  466.16  |
|  `11`  |  4  |  B          |  ti  |  493.88  |
|  `12`   |  5  |  C          |  do  |  523.25  |
|  `13`   |  5  |  C^#^/D^b^  |  di  |  554.37  |
|  `14`   |  5  |  D          |  re  |  587.33  |
|  `15`   |  5  |  D^#^/E^b^  |  ri  |  622.25  |
|  `16`   |  5  |  E          |  mi  |  659.26  |
|  `17`   |  5  |  F          |  fa  |  698.46  |
|  `18`   |  5  |  F^#^/G^b^  |  fi  |  739.99  |
|  `19`   |  5  |  G          |  so  |  783.99  |
|  `20`   |  5  |  G^#^/A^b^  |  si  |  830.61  |
|  `21`  |  5  |  A          |  la  |  880.00  |
|  `22`  |  5  |  A^#^/B^b^  |  li  |  932.33  |
|  `23`  |  5  |  B          |  ti  |  987.77  |
|  `24`   |  6  |  C          |  do  |  1046.5  |
|  `25`   |  6  |  C^#^/D^b^  |  di  |  1108.7  |
|  `26`   |  6  |  D          |  re  |  1174.7  |
|  `27`   |  6  |  D^#^/E^b^  |  ri  |  1244.5  |
|  `28`   |  6  |  E          |  mi  |  1318.5  |
|  `29`   |  6  |  F          |  fa  |  1396.9  |
|  `30`   |  6  |  F^#^/G^b^  |  fi  |  1480.0  |
|  `31`   |  6  |  G          |  so  |  1568.0  |
|  `32`   |  6  |  G^#^/A^b^  |  si  |  1661.2  |
|  `33`  |  6  |  A          |  la  |  1760.0  |
|  `34`  |  6  |  A^#^/B^b^  |  li  |  1864.7  |
|  `35`  |  6  |  B          |  ti  |  1975.5  |

duration: 持续几个base（拍音调持续时间， base时间是1/4拍，125ms）

*返回值*：无。

```py title="playUmusic.py" linenums="1" hl_lines="10 15"
import tqm
import time
from tqe1 import buzzer

base = 125
tune1 = ["C", "C", "G", "G", "A", "A", "G"]
tune2 = ["F", "F", "E", "E", "D", "D", "C"]

for t1 in tune1:
    buzzer.set_note(0, t1, 1)

time.sleep_ms(base)

for t2 in tune2:
    buzzer.set_note(0, t2, 1)
```

## 参考资料
<figure markdown>
  ![大谱表与钢琴键盘对照表](../../img/大谱表与钢琴键盘对照表.png){ width="400"}
  <figcaption>大谱表与钢琴键盘对照表</figcaption>
</figure>
<figure markdown>
  ![黑白键与唱名的对照图](../../img/黑白键%20唱名%20对应关系.jpg){ width="400"}
  <figcaption>黑白键与唱名的对照图</figcaption>
</figure>
<figure markdown>
  ![音调与频率对照表](../../img/音调%20频率.png){ width="400"}
  <figcaption>音调与频率对照表</figcaption>
</figure>
<figure markdown>
  ![国际声学音高记法](../../img/国际声学音高记法.png){ width="400"}
  <figcaption>国际声学音高记法</figcaption>
</figure>