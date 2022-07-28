---
layout: post
author: lipe-dev
---

Tese past few days have been really exciting to me. I have installed the amazing PicoBoot modchip on my GameCube and got really inspired.

My next project will be on my 3DS. Alongside installing a capture card on it, I wanted to also install an external controller mod.

To my dismay, there is no such mod anymore! Loopy used to make and sell one, but it seems he's been out of the market for a while.

I decided to take it upon myself to develop such mod. These are the guiding principles that I want to follow:

- The project **MUST** be open source.
  - First, I don't want this to die with me.
  - Second, I *WILL* need help with a lot of stuff that's outside my realm of knowledge.
  - Finally, I really hope people take this further than I ever had and make it better (so I can also enjoy a better project!)
- The project **MUST** be built with readly available parts.
  - Absolutely NO custom factory made hardware or chips.
  - This will create challenges, but it will also mean anyone can build it at home.
- This project is for, and by, everyone. Let's make it happen!

With these guiding principles in mind, I have already made some initial decisions:

- We will use an Arduino board. A Pro Micro to be precise.
  - Cheap
  - Readily available everywhere
  - Extra cheap if you get a chinese knock off
  - Easy to work with

Even better: I already have two of them lying around.
  
We will support the following controllers:
- GameCube Controller (because otherwise Nintendo/Smash fans would be mad)
- Playstation 2 Controller (simple to work with, and actually has enough buttons to match a New 3DS)

We can plan and add support for more controllers, however the focus should be these two for now.
Mostly, because there are already pretty good libraries we can take advantage of to get these two connected to the arduino board.

- https://github.com/NicoHood/Nintendo For the GC controller
- https://github.com/madsci1016/Arduino-PS2X For the PS2 controller

Are we able to make them both work at once? I don't know. We will find out later.

We will not be adding support for any USB controllers right now. While it is doable, it would require an addiotional piece of hardware to make the arduino capable of acting as a USB host, which will basically double the costs of making this project at home. We can develop this later, once we have at least the 3DS communication working.

You might be thinking: But Lipe, there is no way an arduino will fit inside a 3ds!
And you are absolutely correct.
While there are many boards that use the same chip as the arduino that are much smaller, the Pro Micro is far cheaper and easier to work with.
For now, let's make an external "converter box" that sits outside the console.

Even if we manage to fit an Arduino inside the 3DS, we would need some heavy case modding as well as probably not being able to install a capture card, which goes against the points of "consolizing" the project.

Let's not overthing and overoptmize at first. Let's start simple and get something working, even if it means having 20 wires coming out of the side of a 3DS or something.

That's it for now. Nothing concrete, but these are nevertheless the results of a week's worth of my free time researching.