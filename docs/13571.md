# AVX-512:当比特真正有价值的时候

> 原文：<https://hackaday.com/2022/05/09/avx-512-when-the-bits-really-count/>

对于大多数工作负载，摆弄汇编指令是不值得的。增加的复杂性和代码混淆通常超过了相对适度的收益。主要是因为编译器在生成代码方面已经变得相当出色，而且处理器的速度也快了很多，所以很难通过调整一小部分代码来获得有意义的加速。当你引入 SIMD 指令并需要快速解码大量比特集时，情况就变了。英特尔的[花哨的 AVX-512 SIMD 指令能够以相对较低的定制组装](https://lemire.me/blog/2022/05/06/fast-bitset-decoding-using-intel-avx-512/)提供一些有意义的性能增益。

像许多软件工程师一样，[Daniel Lemire]有许多位集(一系列编码成二进制数的整数/枚举，每个位对应一个不同的整数或枚举)。[Daniel]想知道给定位集中的所有标志，而不是检查是否只存在一个特定的标志(按位 and)。最简单的方法是像这样遍历所有的元素:

```
while (word != 0) {
  result[i] = trailingzeroes(word);
  word = word & (word - 1);
  i++;
}

```

这种天真的版本很可能会出现分支预测错误，您或编译器会通过展开循环来加速它。然而，最新的英特尔处理器上的 [AVX-512 指令集有一些方便的指令专门用于这类事情。指令是*vpcompressed*，英特尔提供了一个方便且令人难忘的 C/C++函数，名为*_ mm 512 _ mask _ compressstoreu _ epi32*。](https://hackaday.com/2018/12/12/intel-announces-faster-processor-patched-for-meltdown-and-spectre/)

该函数生成一个整数数组，您可以使用[臭名昭著的 *popcnt* 指令来获得 1 的个数](https://hackaday.com/2019/06/19/abusing-a-cpus-adders-to-optimize-bit-counting/)。一些早期的基准测试显示，AVX-512 版本使用的周期减少了 45%。您可能想知道，当使用宽 512 位寄存器时，处理器不会降频吗？是的。但即使有降频，SIMD 版本仍然快 33%。如果你想亲自尝试，Github 上有[的代码。](https://github.com/lemire/Code-used-on-Daniel-Lemire-s-blog/tree/master/2022/05/06)