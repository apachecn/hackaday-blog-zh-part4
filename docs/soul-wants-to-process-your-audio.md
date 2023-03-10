# 灵魂想要处理你的音频

> 原文：<https://hackaday.com/2021/01/29/soul-wants-to-process-your-audio/>

抽象是几乎所有计算进步的核心。除非你在制造自己的半导体和拉丝，否则我们都是用构建模块来创造的，从像 CPU 这样的组件，到操作系统功能，到专门的库。就像你不想花时间去解块磁盘记录或为输出设备渲染字体一样，你可能不应该考虑太多音频数据。虽然有一些强大的音频处理库，但一种新的嵌入式语言称为 [SOUL](https://soul-lang.github.io/SOUL/docs/SOUL_Overview.html) (声音语言)，现在已经推出了 1.0 版本，它希望帮助您创建高效的代码来处理音频。

SOUL 的目标是瞄准一个可以在 CPU 上运行，但在 DSP 上更好的运行时。代码的目标是安全和实时的，没有指针、垃圾收集和其他通常会干扰音频处理或安全性的事情。

密码不难破解。以下是将音量减半的示例:

```

processor MinimalGainExample

{
   // declare our inputs and outputs:
   input stream float audioIn; // mono input stream called "audioIn"
   output stream float audioOut; // mono output stream called "audioOut"

// every processor must declare a run() function
   void run()
   {
      const float gain = 0.5f; // a constant to use as our gain factor

      loop // (this just loops forever)
      {
         audioOut &amp;lt;&amp;lt; audioIn * gain; // Read the next input sample, multiply by our
// constant, and write it to our output

         advance(); // Moves all our streams forward by one frame
      }
   }
}

```

您可以看到，处理器是一个基本的线程，可以有本地和全局存储。也有一些图形将不同的处理器与输入和输出组合在一起。

通常，当我们想要处理音频时，我们会转向 PortAudio，就像[Matt]为他的 Quake 示波器端口所做的那样。我们也知道一些使用[纯数据](https://hackaday.com/2012/11/30/guitar-foot-controller-uses-dsp-for-audio-effects/)进行音频处理的项目。