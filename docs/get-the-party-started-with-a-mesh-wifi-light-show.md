# 让派对从网状 WiFi 灯光秀开始

> 原文：<https://hackaday.com/2020/06/26/get-the-party-started-with-a-mesh-wifi-light-show/>

疯狂闪烁的发光二极管可能不是普通办公室环境的理想照明，但它们肯定会给任何聚会增添趣味。因为没有音乐的聚会只是一场会议，所以让两者同步是营造气氛的好方法。当然，你可以简单地推出你的标准 LED 灯条，但这有点无聊，如果你想以同样的方式照亮几个地方，也有点棘手。虽然[Gerrit]可能已经建立了完美的解决方案，他的[*【mu】sic(R)active(Li)lights*](https://hackaday.io/project/172295-murli-a-wifi-connected-and-programmable-music-reactive-light-system)，或 muRLi，这是一组通过 WiFi 同步可编程模式的独立灯。

该系统包括 muRLi 本身作为基站，通过 WebSockets 定义和发送光模式，以及几个 muRLi 节点，这些节点包含一组 WS2812B LEDs 以接收和显示光模式。两者都是围绕 Wemos D1 Mini 构建的，配置为建立 WiFi 网状网络，根据覆盖范围，节点可以连接到基站或其他节点，使系统在任何位置都有足够的覆盖范围。音乐由基站内的 MAX4466 放大麦克风拾取，为系统定位增加了更多灵活性，并对音量和音频频谱进行分析，这也显示在有机发光二极管上。

然而，最好的部分是光模式是如何编程的。[Gerrit]没有将其硬编码到固件中，而是采用模块化方法，用小 ROM 盒式磁带插入 muRLi 基站。卡带本身只包含一个 I2C EEPROM，存储 JavaScript 代码，由固件使用 [mJS](https://github.com/cesanta/mjs/) 进行解释。脚本可以访问网络内分析的音频数据和 led 数量，并可以根据需要动态生成模式。所有的东西都整齐地放置在 3D 打印的外壳中，所有的设计和源文件都可以在项目的 GitHub 页面上[获得——但你可以在休息后的视频中自己去看。](https://github.com/geaz/murli)

如果你不关心无线部分，但喜欢与音乐同步的灯光，看看的普通 MIDI 解决方案[。至于[Gerrit]，我们肯定期待有一天看到他的下一部作品，因为我们也欣赏了](https://hackaday.com/2018/03/31/theres-more-to-midi-than-music-how-about-a-light-show/)[的最后一部](https://hackaday.com/2020/04/22/3d-print-your-way-to-a-bartop-arcade-cabinet/)。

 [https://www.youtube.com/embed/Lw6lD8utsBI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Lw6lD8utsBI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

