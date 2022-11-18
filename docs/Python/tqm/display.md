# 点阵屏 display
## 简介
点阵屏控制主板的点阵屏。它可以用来展示字符串、图像甚至是动画。

## 函数
### 内置图案
#### show(name)
展示内置图案</br>
参数：name，字符串</br>
``` py title="showBuiltinImg.py"
import tqm
import time

# 48副内置图形
images = [
    "heart", "hollow heart", "happy", "sad", "ah", "surprised", "angry",
    "meh1", "meh2", "neutral", "up", "down", "left", "right", "U-turn",
    "yes", "no", "quarter note", "quaver", "music", "rabbit", "fox",
    "snake", "giraffe", " dog", "duck", "turtle", "muscle", "hand",
    "pointing", "telephone", "cellphone", "umbrella", "shirt", "pant",
    "mask", "skull", "robot", "sword", "right arrow", "up arrow", "fu",
    "house", "ok", "pistol", "tank", "sand clock", "trident"] # 内置图案点开查看 (1)

for img in images:
    display.show(img)
    time.sleep_ms(300)

```

1.  内置的表情如下：</br>
    “心”、“空心”、“幸福”、“悲伤”、“啊”、“惊讶”、“愤怒”、</br>
    “meh1”、“meh2”、“中立”、“上”、“下”、“左”、“右”、 “大转变”、</br>
    “是的”、“不”、“四分音符”、“颤音”、“音乐”、“兔”, “狐狸”、</br>
    “蛇”、“长颈鹿”、“狗”、“鸭”、“龟”、“肌肉”、“手”、</br>
    “指向”、“电话”、“手机”、“保护伞”、“衬衫”、“裤”、</br>
    “面具”、“头骨”、“机器人”、“剑”、“右箭头”、“箭头”、“福”、</br>
    “房子”、“ok”、“手枪”、“坦克”、“沙漏”、“三叉戟”


### 自定义图案
#### show(image)
展示自定义图案</br>
参数：image，字符串</br>
``` py title="showMyImg.py"
import tqm

# 参数：1点亮，0熄灭；字符串和点阵的对应关系，从上往下，从左往右。
image1 = "1000100,0000000,0010000,0000000,1000100,0000001"
display.show(image1)

```

### 滚动显示数据
#### display.scroll(value)
