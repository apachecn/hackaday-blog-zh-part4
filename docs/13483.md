# 弯曲使这种六自由度定位器精确到微米级

> 原文：<https://hackaday.com/2022/05/06/flexures-make-this-six-dof-positioner-accurate-to-the-micron-level/>

众所周知，我们认为 flexures 非常酷，我们已经推荐了许多项目，这些项目很好地利用了这些兼容机制。但是当我们看到微米级精度的六自由度定位器[中使用的弯曲部分](https://www.sciencedirect.com/science/article/abs/pii/S0141635922000770)时，我们只需要再深入一点。

The device is known as the Hexblade, and it comes to us from the lab of [Jonathan Hopkins] at UCLA. We have to admit that at times, the video below feels a little like [the “Turbo Encabulator” schtick](https://www.youtube.com/watch?v=jj_rrlZOBrw) — “three identical decoupled actuation limbs arranged in an axisymmetric configuration” may be perfectly descriptive, but it does not flow trippingly from the tongue. Hats off to [Professor Hopkins] for nailing the narration, though, and really, once you get a handle on the jargon, it all makes perfect sense. The platform is supported by a total of six flexures, which look like bent pieces of sheet metal but are actually cut from a solid block of material using wire EDM. Three of the flexures are oriented in the plane of the platform, while the other three are perpendicular to it. The far end of each flexure is connected to a voice-coil actuator that is surrounded by another flexure, this one in a parallelogram arrangement. The six actuators can move the platform smoothly through three linear translations (X, Y, and Z) and three rotations (roll, pitch, and yaw).The platform’s range of motion is limited, but the advantages of using flexures as bearings are clear — there’s no backlash or hysteresis, and the voice coils can control the position of the stage to micron accuracy. Something like the Hexblade would be an ideal positioner for microscopy, and we can imagine an even smaller version, perhaps even a MEMS-fabricated one for nanomanufacturing applications. The original concept of the Hexblade serving as the print head for a fabrication robot for space applications is pretty cool, too, and we’d venture to say that a homebrew version of this probably isn’t out of reach either.

 [https://www.youtube.com/embed/eXULfD94gho?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/eXULfD94gho?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[IraqiGeek]的提示。