# 定制加工泵使数控润滑处于控制之下

> 原文：<https://hackaday.com/2019/06/27/custom-machined-pump-keeps-cnc-lubrication-under-control/>

用足够大的力把两块金属互相摩擦，用不了多久它们就会热到足以引发问题。尤其是当一个是工件，一个是工具边缘时，由于无法管理摩擦产生的热量而产生的问题会让你付出高昂的代价。

处理这种情况的传统方法是向工件泵入大量冷却液，但尽管这种方法有效，但它本身也会产生问题。这就是最少量润滑的来源。MQL 使用在压缩空气流中雾化的润滑剂细雾，这节省了润滑剂，并使切屑更干净，更容易回收。然而，MQL 需要的设备可能很贵，所以[布罗克德]决定在他的数控镂铣机上安装自制的 MQL，效果很好。

下面的视频展示了从原始金属到成品系统的整个过程——如果你只是想看最终测试，可以跳到大约 12 分钟，但要注意你会错过一些高质量的加工。成品泵是双活塞设计，每侧由伺服旋转的凸轮驱动。Arduino 根据当前设置控制电机的速度；泵通过继电器的 g 代码控制打开和关闭。

润滑剂流在视频中几乎看不到，与传统的洪水冷却剂的晃动混乱相反，似乎更适合业余爱好者级的数控设置。需要建立一个数控路由器之前，你建立这个？你能做的比这个差多了。

 [https://www.youtube.com/embed/hyoLF8fZyfU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hyoLF8fZyfU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示，[贾斯珀詹斯]。