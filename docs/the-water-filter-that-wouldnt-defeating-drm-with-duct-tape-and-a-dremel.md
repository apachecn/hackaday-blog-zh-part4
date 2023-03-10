# 用胶带和 Dremel 打败冰箱 DRM

> 原文：<https://hackaday.com/2020/06/14/the-water-filter-that-wouldnt-defeating-drm-with-duct-tape-and-a-dremel/>

我们喜欢在 Hackaday 写关于 DRM 的文章。因为当我们这样做时，通常意味着有人找到了规避供应商强加的强制限制的方法，限制了我们购买后认为是自己的设备的使用。这次出现问题的设备是:内置在通用电气冰箱中的滤水器，通常允许它的“主人”倒一杯清凉的冷水。除了过滤器配有一个 RFID 标签和一个有效期，这将最终拒绝你的小奢侈。如果这已经是一个功能，你可以打赌，它不会让你插入任何任意过滤器作为替代。

被其中的每一个方面激怒，[匿名者] [做了一个网站](https://gefiltergate.com/)来发泄沮丧，最后在之前有同样情况的[的帮助下，把罪魁祸首撕成碎片，绕过了这个问题。事实证明，冰箱带有一个“旁路过滤器”，这只是一片塑料，用来代替实际的过滤器，用来倒未经过滤的冷水。那个旁路过滤器还配备了一个 RFID 标签，所以读取器会将其识别为一个特例过滤器，幸运的是*没有*过期计数器。](https://www.groovypost.com/howto/hack-rwpfe-water-filters-ge-fridge/)

总体想法是取出旁路过滤器的 RFID 标签，并将其放在一个通用的、更便宜的过滤器上，以欺骗冰箱认为它根本没有过滤器，同时仍然享受过滤器的实际功能。但是，如果标签没有放在正确的位置，这可能不是最稳定的解决方案。此外，首先检索标签被证明是棘手的，最初[Anonymous]除了天线垫什么也没有，而标签本身仍然牢牢地粘在塑料片上。

嗯，非常时期需要非常手段——还有 Dremel。[Anonymous]没有取出 RFID 标签本身，而是从旁路过滤器上切下整个部分，这当然不再适合替换过滤器。但事实证明，容纳阅读器的隔间有合适的空间，可以简单地将整个塑料片直接贴上标签，一劳永逸地解决了这个问题。

毫无疑问，DRM 是一个复杂而敏感的话题，从[打印机墨盒](https://hackaday.com/2017/06/04/impression-products-v-lexmark-international-a-victory-for-common-sense/)到[拖拉机](https://hackaday.com/2020/04/21/right-to-repair-tractor-manufacturers-might-have-met-their-match-in-australia/)。当然，可能很难争辩绕过过滤器属于[修理](https://hackaday.com/tag/right-to-repair/)的权利，但考虑到价格溢价，同样很难争辩通用电气这样做完全是为了客户——RFID 标签毕竟不是真的*那么*贵。

(感谢提示，[Brendan Robert]和[Qes]！)