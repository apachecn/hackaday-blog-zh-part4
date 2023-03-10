# 用 BioAmp EMG 药丸监听肌肉

> 原文：<https://hackaday.com/2021/02/15/listening-in-on-muscles-with-the-bioamp-emg-pill/>

有没有觉得你选择的 MCU 错过了读取肌肉电信号的方法？在这种情况下，颠倒实验室的迪帕克·卡特里(Deepak Khatri)[用](https://twitter.com/myupsidedownlab/status/1360296698262659073) [BioAmp EMG 药丸](https://github.com/upsidedownlabs/BioAmp-EMG-Pill)为你撑腰。被描述为一个负担得起的、开源的[肌电图](https://en.wikipedia.org/wiki/Electromyography) (EMG)模块，基于一个 [TL074](https://www.ti.com/product/TL074) 四路低噪声 JFET 输入运算放大器。它的尺寸刚刚超过 32×10 毫米，非常紧凑。

板载运算放大器可确保肌肉运动时捕获的微弱电信号得到充分放大，以便任何微控制器或类似器件的 ADC 能够捕获信号进行进一步处理。当然，使用该模块需要一些如何设置 EMG 的知识，TL074 运算放大器更喜欢 7-30 V 之间的输入电压，即使如此，它也具有所有基本的板载功能，KiCad 项目可通过上面链接的 GitHub 项目免费获得。

此外，【Deepak】还[发推文](https://twitter.com/lorforlinux/status/1360300050400772097)说正在研究一种负担得起的、开源的主动假肢控制器(和人体增强设备)，这让我们对不久后颠倒实验室可能出现的其他项目非常感兴趣。毕竟，我们对[利用生物信号](https://hackaday.com/2016/08/23/all-about-biosignals/)进行黑客攻击并不陌生。