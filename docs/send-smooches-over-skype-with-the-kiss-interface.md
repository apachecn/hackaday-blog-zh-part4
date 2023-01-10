# 通过 Skype 的 Kiss 界面发送拥吻

> 原文：<https://hackaday.com/2018/09/23/send-smooches-over-skype-with-the-kiss-interface/>

[内森]的这个项目当然有一种有趣的直率。他的 Skype“Kiss”界面有一个简单的工作:在使用 Skype 的范围内，尝试创造一种更直观的方式来表达爱意。这一切都来自于一段以聊天程序为主要交流方式的远距离关系。为了寻求一种更直观、更个性化的表达基本情感的方式，[Nathan]发明了一种电容式触摸传感器，当用嘴唇触摸时，它会根据持续时间发送亲吻脸表情符号或红唇表情符号的组合键。

![](img/504bd2216bc12d6c809a47b41c99c27c.png)

电容式触摸感测允许触发传感器，而无需实际将嘴唇接触电极，而[Nathan]通过在 PCB 走线上放置一层透明塑料层来实现这一点。他的开发板使用 STM32 微控制器，软件处理 USB HID 和 STM 的 TSC(触摸感应控制器)功能。因此，该板的元件很少，界面简单，这符合拒绝功能蔓延和专注于简单任务的目标。

显然该单元工作；但是，它实际上能在多大程度上实现其预期目的呢？我们还不知道，但我们知道[内森]似乎拥有他需要的一切来找出答案。无论如何，这都是一个有趣的项目，绝对符合 Hackaday 奖[人机界面挑战](https://hackaday.io/prize/details#four)的精神。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)