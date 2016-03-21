---
layout: post
title: some notes towards a MF scanner camera
date: 2016-03-08 15:42:08 -0800
---

So, one of my great ambitions in life is to make a digital camera. I've made several attempts in the past, but none of them have gotten past the "yes, that's physically possible" stage. There have been some recent developments worth sharing, though.

First, there's the [Aptus](https://www.apertus.org/) who are building a cinema camera from scratch. It's a small team, and they've built several prototypes. What's that, you say? They're professionals with vastly more experience in the area than me or most amateurs? Yes, but it's all open source, so we can look at those designs, and at least learn from them what kind of components they're using, how they're dealing with timing issues, and learn the vocabulary of camera building. Never underestimate the power of knowing the right word; at least, then you'll know what to google.

Then there's [TinyMOS](http://tinymos.com/) which I thought was open souce, but isn't. Still, it's three guys, knocking together a camera. Impressive, but it gives me some idea of the scope of the project; one guy, working for a reasonable amount of time, can find some success.

Then, there's [this linear CCD module](https://hackaday.io/project/9829-linear-ccd-module) on hackaday. For our purposes, it's a working single pixel wide camera. All of the parts can be had for $50 in single quantities, which is _unheard of_. Any other single row detector that I can find is in the hundreds to thousands of dollars, and that's without support equipment. So, how do you turn a single strip of pixels into an image? You move the strip, of course. There was a class of back (may still be) for medium and large format early on in the digital era known as scanning backs, so called because they scanned across the film plane. Now, if I'm reading the spec sheet right, the minimum shutter speed for the TCD1304 would be something like a minute to scan across a medium format piece of film. Read, move the sensor 8 microns, read again. You'd need a slit 8 microns across, as well, to mask off the 200 micron (0.2mm) wide pixels, but that's doable.

A crazy thought just occurred to me. The sensor is ~1cm wide, and cheap. Four of them could fit, side-by-side, and you could divide the movement and the time to record by 4 as well. Alignment would be a bastard. But it's just within the realm of possibility. A fifteen second readout would be a lot nicer than a 60 second one.

I've been sitting here for 10 minutes trying to figure out if there are linear actuators that can handle that fine of movement for reasonable prices, and then I saw that the wikipedia for linear actuators has a DVD player. The head movement is in the range of what we need. Track width on a dvd is 1.1µm, and our pixels are 8µm. So that's fairly possible.

So: several days later, I'm coming back to this, and I've ordered a Mamiya RB67 with several lenses and two backs. I need to order all the parts for the CCD, but first I have to put together a bill of materials. Said BoM will have to include a DVD drive, all the parts from the hackaday post, some 3d-printed adapters, and probably some linear bearings. I'm calling it now: first light before my birthday (in September 😉).
