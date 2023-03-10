# 嗯……模糊贝壳甜甜圈

> 原文：<https://hackaday.com/2020/07/10/mmm-obfuscated-shell-donuts/>

如果你厌倦了写得清晰易懂的代码，混淆竞赛提供了一个很好的场景变化，试图理解他们的参赛作品可能是一个有趣的活动，也是通常脑筋急转弯的有趣替代方案。如果我们碰巧看到关于这个主题的《辛普森一家》剧集，[安迪·斯隆]有一个明显的候选条目:[一个旋转的 ASCII 艺术甜甜圈，格式为甜甜圈形的 C 代码](https://www.a1k0n.net/2011/07/20/donut-math.html)。

代码本身实际上可以追溯到 2006 年，但最近在[Lex Fridman] [在 YouTube](https://www.youtube.com/watch?v=DEqXNfs_HhY) 上发布了一个关于它的视频后，它又重新出现在 Reddit 上，所以我们认为我们应该借此机会进一步关注这件漂亮的艺术品。[Andy]的博客文章详细介绍了旋转数学，以及他如何简单地使用不同像素数量的 ASCII 字符来模拟照明。对于那些更喜欢 C 语言而不是数学符号的人，我们在休息之后添加了一个重新格式化的版本。

当然，代码的甜甜圈形状主要是由于添加了填充符注释，但是让我们面对现实吧，甜甜圈形状只是一个整洁的小添加，如果代码都被压缩在一行中，也不会让人印象不佳。然而，对于实际的 2006 年 IOCCC，[安迪]以他的参赛作品将[向前推进了一大步，你绝对应该试一试。对于一些更令人困惑的外壳动画，查看几年前的流体动力学模拟器](https://www.a1k0n.net/2006/09/20/obfuscated-c-donut-2.html)的[，对于最近的条目，看看我们上个月报道的](https://hackaday.com/2015/03/07/animated-ascii-fluid-dynamics-simulator-is-retro-cool/) [printf Tic Tac Toe](https://hackaday.com/2020/06/05/tic-tac-toe-implemented-in-single-call-to-printf/) 。

 [https://www.youtube.com/embed/DEqXNfs_HhY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DEqXNfs_HhY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



```

int k;
double sin();
double cos();

main() {
  float A=0;
  float B=0;
  float i;
  float j;
  float z[1760];
  char  b[1760];

  printf("\x1b[2J");

  for (;;) {
    memset(b, 32, 1760);
    memset(z, 0, 7040);

    for (j = 0; 6.28 > j; j += 0.07) {
      for (i = 0; 6.28 > i; i += 0.02) {
        float c = sin(i);
        float d = cos(j);
        float e = sin(A);
        float f = sin(j);
        float g = cos(A);
        float h = d + 2;
        float D = 1 / (c * h * e + f * g + 5);
        float l = cos(i);
        float m = cos(B);
        float n = sin(B);
        float t = c * h * g - f * e;

        int x = 40 + 30 * D * (l * h * m - t * n);
        int y = 12 + 15 * D * (l * h * n + t * m);
        int o = x + 80 * y;
        int N = 8 * ((f * e - c * d * g) * m - c * d * e - f * g - l * d * n);

        if (22 > y && y > 0 && x > 0 && 80 > x && D > z[o]) {
          z[o] = D;
          b[o] = ".,-~:;=!*#$@"[N > 0 ? N : 0];
        }
      }
    }

    printf("\x1b[H");

    for (k = 0; 1761 > k; k++) {
      putchar(k % 80 ? b[k] : 10);
    }

    A += 0.04;
    B += 0.02;
  }
}

```

如果你想减慢(或加快)动画，在循环结束时减少(或增加)添加到`A`和`B`的值。让它们保持相同的比例，以保留旋转动画，或者只是摆弄它们，看看会发生什么。

编译时记得用`-lm`链接反对数学库。

[通过[/r/编程](https://www.reddit.com/r/programming/comments/hmfnti/donutshaped_c_code_that_generates_a_3d_spinning/)