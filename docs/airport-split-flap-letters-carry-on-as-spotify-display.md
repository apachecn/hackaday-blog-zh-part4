# Spotify 显示机场对开字母

> 原文：<https://hackaday.com/2020/02/11/airport-split-flap-letters-carry-on-as-spotify-display/>

今天这个在正确的时间出现在正确的地方的故事来自[fabe1999]，当时他正在机场做实习生，这时他们的对开显示屏上的控制器买了一张去南方的单程票。他们正要扔掉成千上万封这些信件，用监视器取而代之，[但是实习生介入了。](https://www.reddit.com/r/arduino/comments/f1buvi/i_finaly_finished_my_airportdisplay_project_more/)

[fabe1999]抓了一捆，带回家，开始让它们重新扇动起来，一次一个字母。阿提尼工作正常，但它真的不够快，以翻转他们的全部潜力，所以[fabe1999]切换到一个 ESP8266。因此，现在 20 个字符中的每一个都有一个 ESP，另一个运行 web 服务器，可以直接输入文本以立即显示。

每个字母使用两个传感器拍打右边的字母。第一个作为开始传感器，检测空白字符的黑色。另一个传感器计数字母，并使 ESP 停止右边的电机。到目前为止，[fabe1999]还没有想出如何识别一个空白字符何时可以保持空白，所以他们暂时回到空白。这无疑增加了丰富、轻快的声音，但这对字母的长期寿命没有好处。您的航班现在出发前往 Post Break Island，letters 将在那里度过他们退休后的一段时间，播放 Spotify 的歌曲。

不会有裂开的襟翼掉到你腿上吧？给你一个提示:你可以自己做翻转动作。

 [https://www.youtube.com/embed/SjHCyaLNxHc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SjHCyaLNxHc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

