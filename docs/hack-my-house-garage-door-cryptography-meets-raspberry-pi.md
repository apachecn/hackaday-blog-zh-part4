# 黑我的房子:车库门密码术遇上树莓派

> 原文：<https://hackaday.com/2019/02/13/hack-my-house-garage-door-cryptography-meets-raspberry-pi/>

今天的故事是一个胜利和失败的故事，一个神秘和冒险的故事…是时候让车库门自动化了。在我的智能家居功能列表中，将车库门连接到互联网是必不可少的。我们的开瓶器内置了互联网连接功能。正如你可能猜到的，当我无法控制设备上运行的软件时，我对将设备连接到互联网非常怀疑。

![](img/12c1851ffe4e9dc5a18466ffcd29c348.png)

车库门由挂在车库墙上的按钮控制。只有一对导线，所以只需要一个简单的继电器来模拟树莓派的按钮按压。我将一个继电器模块连接到安装在车库天花板上的 Pi 上的 GPIO，并用 Python 编写了一个快速而肮脏的测试程序。果不其然，小继电器快乐地发出咔嗒声——但车库门纹丝不动。是时候排除故障了。按钮还能用吗？*打开车库门*是的。现在接力怎么样？*咔嚓…咔嚓*不。

你现在可能已经明白了，但是这个车库门开启器不仅仅是一个简单的瞬间接触按钮。是的，那是一个微控制器，在车库门的按钮上。这种情况需要比简单的万用表更强大的取证设备，所以我转向亚马逊购买了一台 USB 示波器，可以进行一些有限的信号分析。支持 Linux 的设备是必须的，Pico 技术正好符合这个要求。

## 寻找一个我们实际上并不需要的秘密

我的双通道 Picotech 示波器 2204A 终于来了，是时候看看这个车库开门器中有什么样的外星技术了。按钮有两条引线，一条地线和一条五伏线。当按下按钮时，微控制器通过将 5 V 线拉至地，通过该线发回数据。如果这不是 Dallas 1-wire 的实现，这是一个非常相似的概念。

有线协议看起来足够简单，可以用光隔离器再现。我找到了一个合适的芯片并订购了它。对物理接口进行排序后，是时候将注意力转移到数据本身了。

![](img/096872bb420130f40107d1a296941499.png)

那么，打开请求是什么样子的呢？《芝麻开门》？Picoscope 软件能够解码信号，因此对这些设置进行一些模糊处理会得到可重复的结果。UART 速率为 9.6 千波特。38 字节的数据通过网络发送，下一步是捕获其中的几个数据包来寻找模式。

每个数据包都以一个可重复的模式开始，Picoscope 将其解码为 55 01 00。某种标题？源或目的地标识符？到目前为止，我只是没有足够的信息来告诉。除了这种模式，数据似乎是随机的。那么从这里去哪里呢？

![](img/2fc4bbbf7f74f3fe55f1b85764941817.png)

开关下面列出了几个专利号码。专利申请通常包含许多有用的信息，这些信息在其他地方是得不到的。专利也展示了最糟糕的法律言论。涉水通过像 [7，561，075](http://patents.google.com/patent/US7561075) 这样的专利确实偶尔会有收获。它描述了一种围绕简单转换的加密(或混淆)方案。看着专利文件，我怀疑它可能会打破加密方案，并欺骗车库门按钮被按下。

我的下一步计划是用 Python 脚本来处理数据。如果运气好的话，我想我可以重新创建算法，并有可能恢复用于生成数据的秘密。当现实生活的需求侵入黑客的生活时，许多项目都已经脱轨，我也不能幸免。在大约一个月的时间里，这个项目一直停滞不前。我们搬进了房子，我的第一个孩子一周大，是时候让车库门工作了。

![](img/ab51b35cd5e9a0d67f2c0c38ec3902b2.png)

## 欺骗按钮，而不是密码

还记得我们如何开始寻找一个简单的按钮开关吗？原来，有线开启器内置了这样一个开关。将导线焊接到那个小按钮上是最快的实现方式，如果不是最优雅的话。是的，我的解决方案是一个运行继电器的 Raspberry Pi，该继电器桥接有线开启器上的微小物理按钮。

优雅但复杂的解决方案可能是完成工作的主要陷阱。有时你有时间钻研并整合理想的解决方案，但有时你必须完成项目。如果是作弊，而且有效，那就不是…好吧，还是作弊，但是有效，哪个更重要。

我们可以从树莓派的命令行打开车库门。这很有用，但可能有点笨拙。还记得在第一篇文章中，我提到使用 flask 创建 RESTful 接口吗？这是我们可以真正开始的地方。

```

from flask import Flask
import time
import RPi.GPIO as GPIO
app = Flask(__name__)
GPIO.setmode(GPIO.BCM)
GPIO.setup(20, GPIO.OUT)
GPIO.setup(20, GPIO.LOW)

@app.route(&quot;/&quot;)
  def hello():
  return &quot;Hello!&quot;

@app.route(&quot;/moment/&lt;pin&gt;&quot;)
  def moment(pin):
  changePin=int(pin)
  GPIO.output(changePin, GPIO.HIGH)
  time.sleep(.5)
  GPIO.output(changePin, GPIO.LOW)
  return &quot;OK&quot;
if __name__ == &quot;__main__&quot;:
  app.run(host='0.0.0.0', port=80, debug=False)

```

它运行一个基本的 flask 服务器，监听 http 连接。这里，继电器在 GPIO20 上，因此服务器正在等待“/moment/20”的请求，此时，它将 GPIO 翻转为高电平半秒，触发车库门。为了自动运行，我将它保存到了/usr/local/bin/gpio-flask.py，然后在/lib/systemd/system/gpio-flask . service 中定义了一个 systemd 服务:

```

[Unit]
Description=Flask Service for GPIO
After=multi-user.target

[Service]
Type=simple
ExecStart=/usr/bin/python /usr/local/bin/gpio-flask.py
Restart=always

[Install]
WantedBy=multi-user.target

```

告诉 systemctl 启用并启动该服务可以让我们进入正题。拼图的最后一块，让我们在 PXE 服务器上构建一个控制页面。

```

&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;body&gt;
&lt;div style=&quot;text-align:center&quot;&gt;
&lt;form method=&quot;post&quot;&gt;
&lt;input type=&quot;submit&quot; name=&quot;GDO&quot; value=&quot;Cycle Garage&quot; style=&quot;padding:25px 15px;&quot;&gt;
&lt;/form&gt;

&lt;?php
  if ($_SERVER['REQUEST_METHOD'] === 'POST') {
    if ($_POST[&quot;GDO&quot;]) {
      $curl_handle = curl_init();
      curl_setopt( $curl_handle, CURLOPT_URL, 'http://garage/moment/20' );
      curl_exec( $curl_handle );
      // Execute the request
      curl_close( $curl_handle );
    }
  }
?&gt;
&lt;/body&gt;
&lt;/html&gt;

```

我们将在以后进一步扩展这个 PHP 脚本，但是现在它有两个功能。第一个构建并显示界面页面——只有一个标签为“cycle garage”的大按钮。脚本的第二部分仅在收到 POST 请求时起作用。如果“GDO”值出现在请求中，它使用 curl 向我们的 Raspberry Pi 发出命令，打开车库门。这是一条漫长的道路，但它终于奏效了。网页上的一个按钮打开了我的车库门。让我享受一下我小小的胜利…

现在我们已经骗过了车库门开启器，下次我们可以在数据记录和 HVAC 控制上工作。在那之前，祝你黑客生涯愉快！