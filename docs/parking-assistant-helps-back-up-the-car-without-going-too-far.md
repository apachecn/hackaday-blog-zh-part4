# 停车助手帮助倒车，但不会开得太远

> 原文：<https://hackaday.com/2020/09/27/parking-assistant-helps-back-up-the-car-without-going-too-far/>

当然，[Ty Palowski]可以在天花板上挂一个网球，但这意味着爬上梯子，在定位天花板托梁之前在自己身上测试 studfinder，等等。博林。现在他终于有了一个车库，他不会在里面堆满垃圾，不会！他要在里面停一辆大吉普。向后。

[![](img/fba00cf56206c124ff241f0dd68c83a9.png)](https://hackaday.com/wp-content/uploads/2020/09/garage-stoplight-OLED.png) 之前的主人很好心，在车库后面留了一个工作台，这个工作台【Ty】已经自己做好了。[为了确保他在倒车入车库时不会撞到工作台，【Ty】做了一个可爱的交通灯来帮助测量到工作台的距离](https://create.arduino.cc/projecthub/typalowski/parking-assist-stoplight-2794d7?ref=user&ref_id=1451697&offset=0)。绿色表示他很好，黄色表示他应该刹车，红色当然表示以电动工具的名义停车。

灯内是一个 Arduino Nano，它从安装在外壳下的超声波传感器读取数据，并根据汽车的距离点亮相应的 LED。所有[Ty]要做的就是设置让红灯亮起的距离，他可以用旁边的旋转编码器来完成，并在有机发光二极管上确认。黄色和绿色的距离是从红色自动设定的，黄色范围从红色后 24”开始，绿色从黄色后 48”开始。休息时间结束后，播放构建视频。

[不起眼的北美交通信号被广泛认可](https://hackaday.com/2017/08/07/intro-to-the-north-american-traffic-signal/)，因此这是一种适用于各种应用的好方法。教好你的孩子:[让他们从小就知道早上什么时候该起床](https://hackaday.com/2018/05/19/its-not-morning-until-green-oclock/)。

 [https://www.youtube.com/embed/pScwL8NoMn4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pScwL8NoMn4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

