# Python 通过僵尸化的 8 位 AVR 运行

> 原文：<https://hackaday.com/2021/05/23/python-runs-through-a-zombified-8-bit-avr/>

尽管 CircuitPython 很神奇，但它还没有被移植到任何 8 位微控制器上。[Chris Heo]不满足于不能在他的 8 位 ATmega4808 AVR 上使用 Python，所以他想出了一个办法，在他的 PC 上使用 Python 来使它变得“僵尸化”并按照他的意愿弯曲它。

实现这一切的诀窍是 UPDI 接口:一个单线 UART 接口，用于编程和调试 Microchip 的新型 8 位 AVR 微控制器。UPDI 深入微控制器内核，允许您停止和启动微控制器代码的执行，并访问所有板载数据和 I/o。[Chris]意识到这可用于停止 AVR 上运行的任何代码的执行，并使用 pyupdi 库直接控制输出引脚。由于 UPDI 允许他修改 AVR 的 I/O 寄存器，他还能够[闪烁 LED，并使用微控制器 UART 向他的 PC 发送回一条消息](https://www.youtube.com/watch?v=_P3E_l8vl1U)，而无需编译一行代码。

这看起来似乎完全没有必要，但对于太小或太基本而没有 JTAG 接口用于调试的设备来说，这可能是在组装电路中测试和调试外设的最佳方式。我们希望这种方式能够流行起来，并且很想看看有多少芯片可以用这种方式来控制。也许这将使试验一些较新的 AVR 上的可编程逻辑[变得容易。](https://hackaday.com/2021/03/08/avr-configurable-custom-logic-as-a-frequency-divider-at-4x-chips-clock-speed/)