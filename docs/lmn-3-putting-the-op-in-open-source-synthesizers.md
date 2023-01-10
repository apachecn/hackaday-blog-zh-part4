# LMN-3:将“OP”放入开源合成器

> 原文：<https://hackaday.com/2022/06/14/lmn-3-putting-the-op-in-open-source-synthesizers/>

当你看到投入其中的思想和由此产生的工作量时，你遇到的一些项目只是让你敬畏，不仅仅是为了实际的实现，而是围绕它的一切。当它是一个单一开发者的开源项目时更是如此。[Stone Preston]的[synth/sampler/sequencer/DAW-in-a-box*LMN-3*](https://github.com/FundamentalFrequency)完全符合这里的描述，看起来他已经下定决心确保每个人都可以为自己建造一个，提供从外壳到键帽的所有设计文件。

LMN-3 (LMN 在“柠檬”中，而不是“在 [OP](https://hackaday.com/2017/09/05/teenage-engineering-the-raspberry-pi/) 之前”)旨在作为一个独立的便携式数字音频工作站，并围绕一个树莓 Pi 4 构建，用户界面为超像素显示器。UI 本身，以及软件的核心部分，是使用[跟踪引擎](https://github.com/Tracktion/tracktion_engine)创建的，它本身使用 [JUCE 框架](https://github.com/juce-framework/JUCE)，并将典型的合成器、音序器和采样器功能与 DAW 部分结合起来，以处理记录、编辑和混合。剩下的硬件是一个定制设计的 PCB，带有一组功能和键盘按钮，以及一个弯音操纵杆和四个带按钮的旋转编码器，用作主输入处理器。哦，对了，还有一块小木板。

UI 实际上完全由 MIDI 命令控制，Teensy 上的自定义固件相应地翻译来自按钮、编码器和操纵杆的输入事件。这实质上是将硬件从软件中分离出来，并且使用底层的跨平台框架，您也可以在您的计算机上独立运行 UI，并使用您喜欢的任何第三方 MIDI 控制器。或者，就像[Stone]所想的那样，另外使用他创建的硬件模拟器。你甚至可以省去 Raspberry Pi 和软件，把它变成一个纯粹的 MIDI 控制器。如果这听起来很诱人，但你正在寻找有更多旋钮和滑块而不是按钮的东西，请查看 Traktorino 。如果你真的喜欢用鼠标作为输入设备，[浏览器里总会有东西在运行](https://hackaday.com/2020/08/17/gridsound-an-audio-workstation-in-your-browser/)。

 [https://www.youtube.com/embed/h5UmPTttN1s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/h5UmPTttN1s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

