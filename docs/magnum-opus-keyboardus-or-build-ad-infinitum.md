# 巨著键盘，还是无限建造？

> 原文：<https://hackaday.com/2020/09/18/magnum-opus-keyboardus-or-build-ad-infinitum/>

几乎每个接触键盘的人都会遇到这种情况。没有一个商业键盘能满足你的所有需求，所以你开始构建它们。使用它们一段时间，发现问题，建立一个新的键盘来解决它们。很快你就会认为你有足够的用户体验来设计完美的 keeb——你可以带进坟墓的终极巨著 clacker。这一次，发生在[艾登维斯]身上。我们必须说，结果相当不错。但是六个月后还会完美吗？

如你所料，该板使用 Arduino Pro Micro。我们不能肯定地说，但看起来[aydenvis]创建了一个带有第二个 Pro 微型板的插座，该微型板只带有母头。万一板子坏了，这绝对是个好主意。它还具有两个旋转编码器和一对拨动开关，用于在 PCB 之间切换控制器和二级指定。

我们喜欢这个 36 键板中的理念，即当每个手指只能从主排移动一个键的距离时，人体工程学达到最佳状态。这当然需要在固件中编程多层功能，这很容易设置，但要记住却很难。有一个有用的东西是彩色编码的 RGB underglow，我们称之为三明治辉光，因为它是从一对堆叠的 PCB 中间发出的，这些 PCB 漂浮在 7 mm 的支架上。我们只希望能听到那些 jade Kailh choc 开关发出多大的咔嗒声。GitHub 上有电路板文件，所以我们可能需要自己制作。

事实上，我们看到许多 keebs 使用一个或两个 Pro Micro，但这里有一个美味的分裂运行在树莓 Pi Zero W 上。

Via [reddit](https://www.reddit.com/r/ErgoMechKeyboards/comments/is4v8p/a_write_up_of_my_most_recent_36_key_split/)