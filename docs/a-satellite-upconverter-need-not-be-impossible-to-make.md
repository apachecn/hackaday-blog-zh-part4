# 卫星上变频器并非不可能制造

> 原文：<https://hackaday.com/2021/07/31/a-satellite-upconverter-need-not-be-impossible-to-make/>

那些对业余无线电不感兴趣的读者可能错过了它的第一次，因为在过去的一两年里，业余爱好者拥有了自己的地球同步卫星转发器。该卫星名为 Es'hail-2 / AMSAT Phase 4-A /卡塔尔-OSCAR 100，位于东经 25.9°的地球静止轨道上，有一个转发器，上行链路为 2.4 GHz，下行链路为 10.489 GHz。利用为卫星电视设计的 LNB 可以接收下行链路，但对于许多 ham 来说，上行链路是个问题。来自巴西的【PY1SAN】带来了[一个实用且出奇简单的解决方案](https://www.youtube.com/watch?v=E0CKPg8y_Rg)，它混合了奇数个搁板模块和一些手工焊接部件。

上变频器遵循一个非常简单的原理，即在较低的频率下产生无线电信号(在本例中由 435 MHz 发射机产生)，并与来自本地振荡器的信号混频。然后，一个滤波器挑选出混频产物(两者之和)，并将其放大以便传输。[PY1SAN]的上变频器从发射机获取输出，并通过衰减器将其馈入 MiniCircuits 混频器模块，该模块通过放大器从信号发生器模块获取其本地振荡器。混频器输出通过 PCB 带状线滤波器，再通过另一个放大器模块到达功率放大器模块，然后通过同轴馈线到达碟形螺旋天线。

整个系统是由短的 SMA 电缆连接起来的一系列模块，可能很大程度上来自一个全球速卖通订单，而不会有太多的支出。通过 Es'hail-2 进行广播绝非易事，但至少现在它不需要昂贵到不可思议。[连天线都可以不拆银行做](https://hackaday.com/2020/08/04/a-hybrid-helical-antenna-for-the-eshail-2-geosynchronous-repeater/)。

当 Es'hail-2 第一次出现时，我们报道了它。愿它长期为无线电爱好者提供用自制微波设备在世界范围内操作的机会！

 [https://www.youtube.com/embed/E0CKPg8y_Rg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/E0CKPg8y_Rg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

