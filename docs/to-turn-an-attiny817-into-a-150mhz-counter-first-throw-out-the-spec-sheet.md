# 要将 ATtiny817 变成 150MHz 计数器，首先要扔掉规格表

> 原文：<https://hackaday.com/2022/10/14/to-turn-an-attiny817-into-a-150mhz-counter-first-throw-out-the-spec-sheet/>

阅读数据手册通常有两种方式。第一种是从表面上看每一个规格，认为工程师们已经考虑到了一切，并把每个数字作为绝对的限制，以防止魔法烟雾逸出。另一种方法是扔掉数据手册，想怎么试就怎么试，认为工程师尽可能安全地玩。

后一种情况似乎是[推动 ATtiny 方式背后的动机，远远超出了](https://sm6vfz.wordpress.com/2022/10/10/150-mhz-frequency-counter-with-attiny817/)规格表所说的可能性。根据[SM6VFZ]的说法，ATtiny817 的规格表明，12 位定时器/计数器 D (TCD)应限制在微不足道的 32 MHz 最大频率，高于该频率时，应采用计数器的内部预分频器。但是，通过使用 10 MHz 精密频率发生器作为外部时钟，[SM6VFZ]发现略高于 151 MHz 的输入可以 1Hz 精度计数。超过这一点，情况开始发生变化，但从评估板上以明显次优的方式拼凑起来的东西来看，这仍然是相当出色的性能。

我们可以想象这个结果可能会导致一些有趣的项目，因为这个计时器的未记录的限制使它处于多个业余无线电分配的范围内。即使它没有被证明是有用的，那也没关系——看看事情能被推进多远也很酷。而且这也不是我们第一次抓到[SM6VFZ] [劝说一个 ATtiny 做不寻常的事情](https://hackaday.com/2021/01/09/avr-microcontroller-doubles-up-as-a-switching-regulator/)。