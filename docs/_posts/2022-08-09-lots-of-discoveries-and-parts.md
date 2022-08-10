---
layout: post
author: lipe-dev
title: Lots of Discoveries and Parts
---

Hello fellow hackers.

I have been traveling these past 2 weeks due to my wife's job, which has both helped and hindered our progress here. Let me explain.

We currently in São Paulo, Brazil's biggest city. And while traveling, taking care of my kid while working from home while my wife is at the hospital working has taken a toll on my free time and energy, being in such a big city has opened up a few oportunities.

First of all, parts!

This city has a whole neighborhood dedicated to electronics stores, where there are tons of stores that carry whatever electronic component you can ever ask for. (Look up Santa Ifigenia if you are curious).

There I was able to snag a few things that will allow me to move forward:

- A logic level converter module (so we can shift the gamecube's 3.3V output to the arduino's 5V)
- A 16 channel multiplexer (so we can potentially have more outputs, meaning we can support every button on the New 3DS family)
- A breadboard where I can test stuff out
- A pack of jumper wires so I can stop destroying ethernet cables to use their wires
- Some 20 and 26 pins flat cable connectors, which might be the bridge we need to connect the adapter to the 3DS
- Some capacitors and resistors of varying values (we might need to build a poor man's DAC, more on this below)
- A new sponge for my soldering iron
- A 3.3V voltage regulator (the logic level converter needs a 3V3 reference voltage input, and the Pro Micro can only provide 5V)

Now, for the research I have done with the little free time I had these past few days:

## Arduino Analog Output

The analog pins on the arduino are NOT true analog outputs. This clears up the questions I raised in the last post.

They are in fact PWM (pulse wave modulation) pins. What that means for us is:

When you ask for it to provide 50% power, which we would expect to be 2.5V out of the maximum 5V, is in actuality a 5V signal that turns OFF and ON again very fast, 50% of the time OFF, 50% of the time ON.

I am not sure the 3DS will be able to handle a PWM signal for the analog inputs. If someone more knowledgeable than me can explain, I'll be forever thankful. At the moment I do not have access to an osciloscope to figure that out myself.

This is where the aforementioned DACs come in play. Through some capactor + resistor magic we can make a Low Pass Filter and the logic is: the capacitor will charge up while the signal is ON, and provide the necessary voltage when it is OFF. This is obviously an oversimplification, but it is just about as much as I understand this.

The same goes for the 3DS button inputs. However, this is a much simpler case to deal with (we can easily shift the 5V down to whatever the 3DS needs with cheap parts).

## Progress Update

Right now, I have fabricated the GC controller to jumper adapter using an extension cable, and flashed the Pro Micro with the NicoHood/Nintendo sample project, and will atempt to read inputs from the GC controller tonight. I actually got those parts I mentioned above this morning and haven't had the time to play with them yet.

See you next time.

I'll be posting this over at r/3dshacks on reddit, so maybe some people smarter than me will weight in.
