# 西蒙说，但是有了伺服系统

> 原文：<https://hackaday.com/2020/04/07/simon-says-but-with-servos/>

如果你能抓住任何你想操纵的机械装置，随心所欲地移动它，然后让它精确地模仿你的动作，生活会变得容易多少？如果你能给一个类似 MIDI 的命令，告诉它在特定的时间内移动到某个特定的位置，会怎么样？不再感到惊讶，因为[彼得格拉博]已经将这个想法变成了现实。

只需一根电线，一个 Arduino，和一些非常简洁的代码，[彼得]就可以让这个伺服做他想做的任何事情。首先，他告诉 Arduino 所需的持续时间，单位为每秒帧数。然后他抓住喇叭，随心所欲地转动它——它甚至可以控制不同的速度。伺服记录，然后模仿运动，就像他们被制造出来。

整个操作比你想象的要简单得多。正如[peterbiglab]在中断后的视频中演示的那样，由于电机转子上的内部电位计，伺服系统知道自己的位置。如果您在控制板上找到 pot 输出引脚，并从那里将一根电线接入 Arduino，您就可以使用该信息轻松校准和控制伺服位置。这种控制有很多可能性。你会用它做什么？请在评论中告诉我们。

如果你想一次尝试一堆伺服系统，不妨[为自己建造一个小小的测试控制台](https://hackaday.com/2020/01/05/space-saving-servo-tester-console-looks-space-worthy/)。

 [https://www.youtube.com/embed/QR_Oo8hpsL4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QR_Oo8hpsL4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



通过 [r/Arduino](https://www.reddit.com/r/arduino/comments/fuud8a/i_modified_a_servomotor_that_now_learns_how_to/)