# 短波收音机接收边带

> 原文：<https://hackaday.com/2021/09/29/shortwave-radio-picks-up-sideband/>

随着将大部分无线电接收器作为 PC 的一部分的推动，拥有独立的通信接收器可能看起来很奇怪，但[【OM0ET】回顾了他最近拿起的一个](https://www.youtube.com/watch?v=M6Hgx93mleA)，一个 ATS25。内部并不多:一个电池、一个扬声器、一个编码器和一个提供射频肌肉的 Si4732。

似乎接收器是相当宽带，这可能是一个问题。[OM0ET]建议在天线中增加选择性，或者增加额外的电路板用作带通滤波器。

这个设计很简单，我们相信你可以很容易地破解这个单元来做不同的事情。大多数覆盖停止在 30 兆赫，但有一个调频波段，所以我们想知道你是否可以让这个东西在其他频率上工作。

显然，Arduino 部分很容易被破解。对于价格，我们都对触摸屏和构造印象深刻，但对射频滤波的印象可能不太好。另一方面，小巧的外形非常适合背包或便携使用，而且也不贵。在实践中，它看起来确实工作得很好。

我们见过类似的自制收音机[使用相同的芯片组](https://hackaday.com/2020/02/12/all-band-radio-uses-arduino-and-si4730/)，或者至少[使用类似的芯片组](https://hackaday.com/2020/03/02/multi-band-receiver-on-a-chip-controlled-by-arduino/)。

 [https://www.youtube.com/embed/M6Hgx93mleA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/M6Hgx93mleA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

