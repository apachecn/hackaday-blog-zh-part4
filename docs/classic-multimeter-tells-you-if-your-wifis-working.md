# 经典万用表告诉你你的无线网络是否工作

> 原文：<https://hackaday.com/2022/02/22/classic-multimeter-tells-you-if-your-wifis-working/>

调试网络问题并不容易；许多系统管理员花了几个小时试图找出客户机和服务器之间的许多链接中的哪一个是错误的。有几个清晰的指示会有所帮助:如果您可以显示互联网连接正常，这已经将问题缩小到服务器，或者最有可能的是客户端计算机。

在听了太多次“互联网是否正常”之后，[威士忌酒吧]决定将[做成一个清晰可见的指示器，以显示本地上行链路](http://www.whiskeytangohotel.com/2022/02/simpson-260-vom-answers-is-internet-up.html)的状态。他用他父亲的老式辛普森 260 VOM 作为显示器，如果互联网开通，它的大型模拟指示器会指向一个稳定的值，如果互联网中断，它会前后摆动。显示的确切值由几台不同服务器的平均 ping 时间决定，因此您也可以判断连接是否比正常情况下慢。

ping 时间由连接到 WiFi 的 ESP8266 测量，它检查预定义的 web 服务器列表，并每 15 秒计算一次平均 ping 时间。然后产生一个 2.5 V 范围内的模拟值，并由电表测量。老式模拟电表的平稳运行与当今 WiFi 不稳定的问题形成了鲜明对比。

虽然模拟万用表肯定[有它们的用途](https://hackaday.com/2017/11/08/why-you-shouldnt-quite-forget-the-moving-coil-multimeter/)，但我们第一个承认，我们的经典万用表没有发挥出它们应有的作用。像[威士忌酒酒店]那样重新利用它们是为下一代保留这些传家宝的一种巧妙方式。当然，如果你没有模拟万用表，你也可以[为你的 ping 表](https://hackaday.com/2022/02/09/that-clock-on-the-wall-is-actually-a-network-ping-display/)使用模拟时钟。

 [https://www.youtube.com/embed/Wpw3AmSZErc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Wpw3AmSZErc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

