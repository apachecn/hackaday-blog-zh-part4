# 自动百叶窗可以是一个便宜和容易的建设

> 原文：<https://hackaday.com/2022/06/16/automated-blinds-can-be-a-cheap-and-easy-build/>

百叶窗可以很好地遮挡阳光，但在这个计算先进的时代，不得不起来打开和关闭它们变得令人厌倦。[The Hook Up] [决定将他家的百叶窗自动化，而不是](https://www.youtube.com/watch?v=1O_1gUFumQM)，用一些常见的现成零件将它们连接到物联网。

基本想法是使用步进电机来转动倾斜杆，从而打开和关闭百叶窗。用单极步进电机打开百叶窗的早期尝试被证明是不成功的，当弱电机在 5 伏电压下运行时不能完全关闭百叶窗。不想扔掉手头的硬件，电机改为双极运行。然后将它们连接到 DRV8825 驱动板上，以 12 伏电压运行，以提供更大的扭矩。

解决了机电方面的问题后，很容易将电机驱动器连接到基于 ESP8266 的 NodeMCU。物联网设备可以通过网络轻松远程控制电机。

这种建筑成本很低，每个百叶窗大约 10 美元。相比之下，商业选择要花费数百美元，这是一个很好的节省。我们以前也看过[The Hook Up]的其他作品，比如他的创意 [Flex Seal screen build](https://hackaday.com/2022/06/10/making-a-projector-screen-out-of-flex-seal-works-okay-kinda/) 。休息后的视频。

 [https://www.youtube.com/embed/1O_1gUFumQM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1O_1gUFumQM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

