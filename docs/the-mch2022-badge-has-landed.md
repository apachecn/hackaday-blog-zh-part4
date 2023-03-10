# MCH2022 徽章已登陆！

> 原文：<https://hackaday.com/2022/05/04/the-mch2022-badge-has-landed/>

在撰写本文的欧洲，随着春天慢慢进入夏天，温暖的天气提醒人们，黑客营地的夏季即将到来。今年最大的欧洲赛车将是 7 月底的荷兰 MCH2022，为了吊起我们的胃口，他们公开了他们徽章的一些细节。和过去的荷兰营地一样，这是一个令人印象深刻的建筑。

由于这是来自 [badge.team](https://badge.team/) 的另一件作品，它有预期的 ESP32 模块，但在它旁边的优雅设计的 PCB 上有一个 RP2040 和一个晶格 ICE40UP5K FPGA。ESP 运行 badge team 固件，甚至包括与原始 SHA2017 badge 的向后兼容性，RP2040 将一切联系在一起，并提供大量 USB 外设，FPGA 运行用户代码。从正面看，徽章具有 Game Boy Advance 风格的外形，带有大型彩色 TFT 屏幕和常见的操纵杆和按钮。其他外设包括一对可寻址 led，一对来自博世的漂亮传感器，以及一个 16 位立体声音频通道，当没有连接耳机时，它甚至可以为一个小型的板载单声道扬声器供电。

硬件可能很光滑，但正是[badge . team 固件](https://hackaday.com/2019/02/20/badge-team-badges-get-a-platform/)让这款产品与他们之前的所有产品一样特别。它提供了轻松编写应用程序的机会，无论是在 ESP32 的 MicroPython 中，还是作为 FPGA 的有效载荷，它的特别之处在于它带有一个在线应用程序商店，可以从那里下载所有的应用程序。我们被告知，它将能够运行一系列的模拟器，所以我们真的很期待在活动中看到最终版本。与此同时，他们发布了一个演示视频，你可以在休息时看到，如果你好奇，你可以[看看它的 SHA2017 徽章祖先](https://hackaday.com/2017/05/08/the-sha2017-badge-revealed/)。

 [https://www.youtube.com/embed/-yk3I0oce4k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-yk3I0oce4k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

