# Kinesis + Teensy = QMK 优于您的键盘

> 原文：<https://hackaday.com/2021/08/05/kinesis-teensy-qmk-advantage-over-your-keyboard/>

早在 2013 年，[迈克尔·斯坦伯格]创造了一种被亲切地称为斯坦伯格控制器的东西:一种替代原始 Kinesis Advantage 的键盘控制器，这是人体工程学领域几十年来的宠儿。无论你是在建造一个新的 keeb，你已经得到了一个坏的 Kinesis，或者你只是想在这个东西上运行 QMK，并不介意弄脏你的手，[有一个新的 Stapelberg 控制器在块上](https://michael.stapelberg.ch/posts/2020-07-09-kint-kinesis-keyboard-controller/)。这叫 kinT，代表 Kinesis + Teensy。

[Michael]打造 kinT 是为了应对 2017 年问世的 Advantage 2，它改变了 thumb 集群连接主板的方式，从焊接电缆到 FPC 连接器。尽管最初的 Stapelberg 控制器是在 Eagle 中构建的，但这个控制器是在 KiCad [中完成的，并且是开源的，还有固件](https://github.com/kinx-project/kint)。你可以在这个板上使用 Teensy 4，但是如果你没有，不要担心——kinT 可以向后兼容几乎所有的 Teensy，它甚至可以在原有的优势上工作。

你是否在犹豫要不要全力以赴？查看[我对最初的 Kinesis Advantage](https://hackaday.com/2020/03/03/inputs-of-interest-my-first-aggressively-ergonomic-keyboard/) 的深入评论，它已经用了将近 20 年，仍然像新的一样。但是[不要等到重复性压力损伤完全恢复。相信我。](https://hackaday.com/2021/07/22/avoiding-repetitive-stress-injury-invest-in-yourself-now-or-pay-later/)