# 把我传送到 PCB 太空船上

> 原文：<https://hackaday.com/2019/10/19/beam-me-up-to-the-pcb-space-ship/>

如果有人能想出办法把它挂在脖子上，这个项目将与#BadgeLife 完美契合。受到《星际迷航》中[星际飞船企业号](https://hackaday.io/project/162654-pcb-3d-startrek-enterprise)的启发，【bobricius】决定设计并组装一个微型宇宙飞船 PCB 模型，配有 40 个由 ATtiny85 控制的闪烁 led。

虽然设计使用 0603、0802、3014、4014 和 0805 LEDs，但由于最小的 led 可能难以焊接，因此可以进行一些替换。灯光效果包括一个绿色激光器、等离子线圈、一个带有滚动蓝色发光二极管的偏转器，以及宇宙飞船的主板和舰桥。

led 由 charlieplexing 控制，这是一种用相对较少的 I/O 引脚驱动 LED 阵列的技术，不同于传统的多路复用。查理多路复用允许 *n* 引脚驱动*n²n*led，而传统多路复用允许 *n* 引脚驱动(*n/2)²*led。(这是我们见过的对 Charlieplexing 的最好解释。)

尤其是编译好的固件在 MCU 上运行时，PCB 模型的显示效果令人印象深刻。

唯一的问题是。你的星舰企业号实际上不能飞。

 [https://www.youtube.com/embed/jU-paBWy9zs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jU-paBWy9zs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)