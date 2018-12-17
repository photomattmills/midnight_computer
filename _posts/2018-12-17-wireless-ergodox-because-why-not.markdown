---
layout: post
title: wireless ergodox because why not
date: 2018-12-17 11:45:25 -0800
ogimage: ""
description: "some pictures for yr eyes"
---

I've done kind of a lot of keyboards at this point. I made two [Atreus](https://atreus.technomancy.us/) from a kit, modified one to be wireless, and then almost completely rebuilt it after stepping on it and crushing the case. Then I got into Ergodox, and built one of those from an [ok kit](https://input.club/devices/infinity-ergodox/) from Input Club. Finally, I decided 40% boards are not really for me, so I made a [compact wireless planck](https://www.instagram.com/p/BjgfmlxHbZT/) that didn't work terribly well ergonomically. 

So, I have a lot of boards, and they're all of the microcontroller with matrix variety. They were all kits because I thought hand-wiring was a pain in the ass, and large PCBs tend to be expensive to have custom-made for a one off. But, time moves on and I'd heard about what's called 'hand wiring,' where you don't need a pcb to hold the switches. I got some plates for an ergodox from a european company for a steal, and bought switches from Mouser. Then, this fall happened, in which I was super busy with work and travel and so nothing got done. 

Thinking about it, though, that's not true; I designed the thing and managed to solder all the components together before I went on vacation in October. I used an adafruit feather M0 w/bluetooth that I had sitting around, since they're great for wireless keyboards, and the Boldport Ixpando, which is a breakout for the microchip MCP23017, a 16-bit i2c shift register. I read a couple guides on hand-wiring, bought a bunch of diodes, and threw it together. The bottom plates are some 3/16" aluminum I just happened to have laying around. Brass standoffs and M3 machine screws hold the key plates to the base. 

![Matrix Wiring](https://midnight.computer/images/ergodox/IMG_2534.JPG)
![More matrix](https://midnight.computer/images/ergodox/IMG_3188.jpeg)
![](https://midnight.computer/images/ergodox/IMG_2624.jpeg)

After I got that done, it sat for a couple months while other matters occupied my time. But, eventually I got back to it and modified my existing wireless keyboard firmware to work with the shift register. That's a project that's still ongoing, because there's still a tiny bit of lag; 25ms to scan is a little too long. I've wrestled with it quite a bit just to get it to work, but it finally does. 

![](https://midnight.computer/images/ergodox/IMG_3233.jpg)
![](https://midnight.computer/images/ergodox/IMG_3232.jpg)

(If you look closely you can see that the battery is disconnected; that's because I was debugging, but it works just fine. I do need to put in an on/off switch...)
