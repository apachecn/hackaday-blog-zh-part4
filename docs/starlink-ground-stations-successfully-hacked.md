# Starlink 地面站成功入侵

> 原文：<https://hackaday.com/2022/08/14/starlink-ground-stations-successfully-hacked/>

比利时安全研究员[伦纳特·伍特斯]已经让他自己的代码运行在 Starlink 的“漂亮的 McFlatface”卫星终端上，你也可以！有问题的黑客是一个[“modchip”，带有一个 RP2040 和一个 MOSFET，可以撬动电源轨](https://github.com/KULeuven-COSIC/Starlink-FI)，当它验证固件的有效性并完全绕过这种保护时，主 CPU 就会断电。[Lennert]之前已经想出了如何让[直接从 eMMC](https://hackaday.com/2021/07/07/starlink-terminal-unit-firmware-dumped/)转储 Starlink 固件，并且有能力上传回来，这种关系就结束了。这是在 DEFCON 上的一次演讲，[你可以在这里查看幻灯片](https://github.com/KULeuven-COSIC/Starlink-FI/blob/main/GlitchedOnEarth_slides.pdf)。(PDF)

mod 芯片本身是一个可爱的作品，被定制成适合 Starlink 的主板，并充分利用了 RP2040 的 Pio，这可能是微控制器的超级能力。

[Lennert]说他向 Starlink 提交了故障攻击，他们采取了一些预防措施，使故障更加严重。特别是，[Lennert]在 Starlink 设备上触发了他的 USART 端口计时，因此 Starlink 将其关闭。但这并不是说他不能触发其他一些与时间相关的数字信号，所以他选择了 eMMC 的 D0 数据线:没有它他们就无法启动，所以这次黑客攻击可能是最终的。这里没有反对 Starlink 的阴影。几乎不可能保护一个设备免受放在他们工作台上的攻击者的攻击，[Lennert]得出结论说，他没有找到容易摘到的果实，并对他必须如此努力才能生根留下深刻印象。

你能用这个做什么？还不多。但原则上，它可以用来探索 Starlink 网络的其余部分的安全性。正如《连线》中的[报道，Starlink 说他们有一个纵深防御系统，仅仅进入网络并不能让你走得很远。我们走着瞧！](https://www.wired.com/story/starlink-internet-dish-hack/)

谢谢[jef]的提示！