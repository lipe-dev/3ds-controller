---
layout: post
author: lipe-dev
title: Research continues, and I found something cool!
---

# Research continues, and I found something cool!

I found out a lot of things today. And here is a summary of it all.

## Not enough pins!

Turns out, the arduino pro micro will not work for us. It does not have enough Pins to communicate with the 3DS. We will need all those pins:

```
- DPAD UP
- DPAD DOWN
- DPAD LEFT
- DPAD RIGHT
- A
- B
- X
- Y
- L
- R
- ZL
- ZR
- CIRCLE PAD X
- CIRCLE PAD Y
- C STICK X
- C STICK Y
- START
- SELECT
- HOME
```

A grand total of... 19 pins!
And that's not even all pins we will need. We will still need a few(2 or 3) INPUT pins where the controller connection will go in.

I am stumped right now. We might need something like a multiplexer. Fortunately, they are VERY cheap. 
I will order some and run some tests. This, along other parts @NicoHood describes in his project will only add cents to the overall cost, so no big deal.

## Some people have, obviously, been there before!

After some clicking around, I found out about some old projects that achieve most of what we are trying here. We will definitely be pulling some info from those! The main one is this:

- [dekuNukem/gc3ds](https://github.com/dekuNukem/gc3ds)

This has some very valuable info about what the 3DS expects in terms of signals and voltages! For instance, a Circle Pad outputs voltages from 0 to 1.3V.
I am not sure we can achieve that with the arduino's analog pins. Needs more research.

And that's it for now.

I think it's time for me to start actually testing some stuff out. I just need to order some parts now.
