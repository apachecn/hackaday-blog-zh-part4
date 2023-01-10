# 反射训练器测试运动员

> 原文：<https://hackaday.com/2018/12/15/reflex-trainer-puts-athletes-to-the-test/>

在当今时代，成为顶级运动员是一项全职工作。运动员不再只是在他们指定的运动项目上练习。他们接受力量训练、全面营养计划、有氧运动，甚至反射训练。

反射训练包括一系列节点，运动员必须在点亮时识别这些节点，并触摸它们以关闭它们。通过快速触发它们，运动员必须努力识别点亮的节点，然后将其关闭。 [TrainerLights 就是这样一个系统，围绕 NodeMCU 平台](https://www.hackster.io/hongo2/trainerlights-training-system-to-improve-athletes-reflexes-96d988)构建。

该系统至少由四个灯组成——一个作为服务器，其他作为节点。每个灯都包含一个通过 WiFi 进行通信的 nodeMCU 板，而服务器有一个附加的板-作为控制系统的 WiFi 热点。

打开灯后，教练用智能手机连接到服务器，并根据所需的锻炼制度配置照明顺序和时间。然后，服务器与照明节点通信，照明节点以指定的时间间隔点亮 led。运动员必须通过在节点上滑动来清除灯光，这些节点通过超声波近程传感器检测运动员的手。灵敏度是可配置的，以允许系统从远处的波或运动员的直接触摸中触发。这允许多种训练用途，从[网球](https://photos.google.com/share/AF1QipMeVv3YXNE0dztrYXWW7n44rvFKRjXNqWN3rwHZMfjZVM0TYIakx9QQQQjG82Vv5w?key=eERaWG4zazZITUUzTnlIdDhYYnJ5Tzcyb0pNVWZR)到[跆拳道](https://photos.google.com/share/AF1QipO3EtDuZpmNq1LIDlrxi2PwLA_PeNhOeO1ezYz3MvaEXTxVRBhGy-1B16jBVxFgjA/photo/AF1QipMd_joySyMKy8ee7PpF25z-r5wJuq1o3ou25PoD?key=Sk5CMjR6X1ZKLThBYzRwWEZTSFZNS3pzNUlHSnJB)。

有了一个 3D 打印的箱子和零件，你可以从任何好的制造商供应商那里获得，这是一个你可以在一个周末处理的项目，以增加你自己的训练制度。

我们在这些地方看到了大量的运动员——比如这个训练短跑运动员的循线机器人。休息后的视频。

【感谢 Baldpower 的提示！]

 [https://www.youtube.com/embed/fPKZi_MTf9c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fPKZi_MTf9c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

