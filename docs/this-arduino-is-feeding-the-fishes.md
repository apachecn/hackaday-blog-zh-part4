# 这只 Arduino 正在喂鱼

> 原文：<https://hackaday.com/2019/07/02/this-arduino-is-feeding-the-fishes/>

鱼很容易作为宠物饲养，只需要定期喂食就能让它们在中短期内保持快乐。如果你要去度假，知道你的宠物得到了照顾是很好的，但是找个人来承担家务可能很难。[Trevor_DIY]不需要担心这一点，然而——他已经建立了一个自动进料器来处理这项工作。

该构建使用 Arduino Uno 作为大脑，唯一需要的额外硬件是步进电机和驱动器。步进电机驱动一个 3D 打印的轮子，轮子上有 14 个插槽，每个插槽都可以容纳一餐鱼。这使得喂食器可以在需要注意之前一整天输送两餐。

进料器被配置为供应早餐，然后在 8 小时后供应晚餐，然后在早餐再次到来之前等待 16 小时。无需使用实时时钟，只需使用 Arduino 的内置延迟功能即可。虽然它不是超级准确，但这应该足够接近一周，以保持鱼活着。我们很想知道它会随着时间漂移多远。

总的来说，这是一种快速而整洁的方式，让宠物继续生活，没有太多的麻烦。宠物喂食器是一个受欢迎的项目，因为它们解决了世界各地的主人面临的一个共同问题；[这个甚至可以处理湿猫粮](https://hackaday.com/2019/03/22/auotmated-cat-feeder-handles-wet-food-with-aplomb/)。休息后的视频。

 [https://www.youtube.com/embed/ya5smFiaK54?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ya5smFiaK54?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

