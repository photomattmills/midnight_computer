---
layout: post
title: senoko pt 2 and other notes on higonokami bringup
date: 2016-11-27 00:24:16 -0800
---

So, over the last couple weeks, I've been making progress on the new laptop, which I've been calling 'higonokami', after the Japanese style of pocket knives. I have this thing for naming my laptops after simple machines. Anyway, progress has been steady. 

First, building the senoko. I recieved my boards from OSHpark and they were great. I still have two extras and no idea what to do with them. The stencils I ordered at first were for the wrong version of the board, so I had to re-order them. It was just as well that I was delayed a couple days, until the weekend. I started working on the board at around 9pm saturday and took it out of the oven at 2am sunday. It programmed immediately but there were a few solder bridges I didn't catch that caused it not to work right away. 

Before I get too far into the bringup, I'd like to diverge into talking about placing all those components by hand, which took most of 4 hours. I was working from the BOM and trying to place all the components of one type at once; all the 100k resistors, all the FETs, etc. About halfway through, I realized it would have been quicker to organize all the parts first, and then go over the board in one pass and place them by reference as I found them. I got it done, anyway. 

So, back to the bringup. I got it programmed, and then had what I thought were issues with the gas gauge. As it turns out, it just takes a little time to settle down. But, I decided I'd replace the one on the board with a spare, and try that. After that had the same issues, I started messing with the battery connector, and ended up shorting it, damaging the gas gauge and a current sense resistor. I thought it was just the gas gauge, since it started showing new worse symptoms, so I ordered a couple more and didn't work on it for a week while I waited for parts. 

When the new chips came in, I got one installed with my reflow setup (hot air is an essential tool), and saw it having the same issues. So, I went to the schematic, and stared at it for a while. I saw that maybe the current sense resistor had something to do with something, so I tried shorting it, and suddenly the GG came to life. A few minutes and a spare resistor later, it was working fine, and the battery was charging. Shortly after that, I was able to unplug it from the AC adapter, and confirm everything was working. 

So, with that done, I've been focusing my efforts in two areas: getting the software setup reasonably squared away, and getting an adapter made for the LCD I'm using. The board I've made is just a passthrough to adapt one cable type to another. I'm using a comercial board with the same chip as the eDP adapter that came with the novena kits. 

The software has been a little more complicated. This is an ARM laptop, armhf arch. There are some things precompiled, for example Chromium is available pretty easily, but Atom is not, and some other creature comforts aren't here. There's no onepassword port, even to Linux. Most of the debs I've been getting from the ubuntu 14.04 repos. Also, there's no lightroom equivalent, so I may have to get creative. 

In near future: a sheet metal case for this beast, clamshell, just like any other laptop. Friction hinges from McMaster Carr make that possible. Also, the LCD bringup is soon. That'll pretty much finish this off. I'd like to have it done in time for our trip to oklahoma. We'll see if that actually happens. 

