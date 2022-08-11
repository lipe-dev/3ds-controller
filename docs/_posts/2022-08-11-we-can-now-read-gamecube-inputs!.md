---
layout: post
author: lipe-dev
title: We Can Now Read GameCube Inputs!
---

That's it, the first milestone has finally been reached! :party-popper:

Let's talk about it.

Over at [https://github.com/NicoHood/Nintendo](NicoHood/Nintendo) there are some schematics that are frankly a bit confusing to me, but I got through.

First of all, the Pro Micro does not have a 3.3V output, so I had to buy a 3.3V voltage regulator. Very cheap and totally worth not having to build my own (even though it's a very simple circuit).

The 3.3V output is needed to power the logic level converter. Actually, not power, it is called a "reference voltage" that it uses to "know" what voltage the signal will be converted to.

That's basically the only hurdle we had to actually go through... but for 2 days my circuitry simply did not work.

I tried everything, New pro micro, new wires, disassembled everything and put it back together with double care... nothing.

You can follow this saga in [https://github.com/NicoHood/Nintendo/issues/54](this issue, where Skuzee tried to help) and finally in [https://www.reddit.com/r/arduino/comments/wle3h3/has_anyone_had_success_reading_a_gamecube/](this reddit thread) where my stupid mistake was finally revealed.

Turns out not all rails on my breadboard are connected all the way through. A couple jumpers did the trick.

Here is the first pic of the project:

![first version that does something](https://github.com/lipe-dev/3ds-controller/blob/main/docs/_posts/img/43238632-215d-4ae4-84d7-1a7c849f738a.jpg?raw=true)

What a mess! But at least, it's a mess that does something.
