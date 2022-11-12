# 点阵屏
## 简介
颜色传感器，获取颜色的相关数据。

## 函数
### 内置图案
#### colorSensor.getColor(port)
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
