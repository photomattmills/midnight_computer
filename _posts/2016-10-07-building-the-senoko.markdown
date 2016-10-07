---
layout: post
title: building the senoko power board
date: 2016-10-07 12:10:33 -0700
---

TL;DR -- board is shared on OSHPark [here](https://oshpark.com/shared_projects/x3IpMg2U), BOM is at mouser [here](http://www.mouser.com/ProjectManager/ProjectDetail.aspx?AccessID=6572045792), and stencils from OSHstencils (you should be able to export the cream layers from the KiCAD versions of the board [here](http://bunniefoo.com/novena/novena-accessories-kicad.zip)).

So, my laptop died over the weekend, not permanently, but enough to get me thinking. The failure was in a tiny component that I could probably fix, if I knew what it was and could source it. This got me thinking about the [Novena](https://www.kosagi.com/w/index.php?title=Novena_Main_Page), which is a completely open source laptop, built to be as open as possible. It's not a fast machine, but for most of my uses I really only need a typewriter with some sort of UNIX-like environment, usually debian or ubuntu. So, somewhat spurred on by the ennui of a broken machine, I ordered a board.

The first problem with this scenario is that the battery board, Senoko, the thing that handles charging and power management, is not available. Since it's open source, that's fixable.

The board is only four layers, so we can have it made by OSHPark. I downloaded the [gerbers](http://bunniefoo.com/novena/pvt2_release/gerbers-senoko_pvt1.zip) from the site, and uploaded the file directly. I chose OSHPark because I've used them in the past, and DirtyPCBs' 4-layer non-custom size is 2cm too small in one dimension. There are two plated slot holes, which OSHPark doesn't support, but they're mounting tabs that can be cut to fit the round holes. The rest of the board is standard, and doesn't present any issues.

The second part, ordering the BOM, is a little trickier. Most of the components are cheap, and so we get enough to get at least the 10 item discount. Some things, I only ordered 1 of; if you want to make two, it'll cost an extra $30 or so at this step (only double the components that aren't already doubled because of quantity discounts), and double the time at assembly. There are a few substitutions from the original BOM: both of the ferrites were EOL'd, so I found equivalents for them. The barrel jack connector isn't identical, but the closest mouser had, and should work. One of the fuses wasn't available, but a close equivalent was. Finally, the supercap was also EOL'd, so it's replaced with a similar one (slightly more capacitance, but it should work, since it's a power storage device in this circuit).

The stencils are another thing. You'll need to open the board in KiCAD or Altium (if you have altium and know how to use it, you know how this works). Then go to File->Plot, and select the two cream layers, and then export them. Then follow the directions to upload them to OSHstencils, and order them.

Board assembly is, at this time, an exercise for the reader. There are plenty of good tutorials out there if you haven't ever done surface mount work before. None of this is too terrible; as long as you get the components roughly on the pads, the surface tension of the molten solder will move them into place. The only real hair-shirt part of this project will be hand-placing 226 components with tweezers; it's a lot to place by hand. The board is small enough that you can get it in a toaster oven for reflow, and there are few enough components on the bottom that they can be hand soldered. I'll probably use hot air for the bottom, just to save myself trouble.

So, that's it. $220 worth of material and you can put it together, assuming you have access to a reflow oven, solder paste, and the sundry tools needed. Probably the MVP for that is a halogen work light and Chip-quik low temp solder paste. Lovely stuff, but beyond the scope of this post. Go forth and google.
