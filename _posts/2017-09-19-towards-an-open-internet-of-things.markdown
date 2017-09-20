---
layout: post
title: towards an open internet of things
date: 2017-09-19 21:41:11 -0700
ogimage: ""
description: "some ramblings about stuff"
---

<div style="width: 500px;" class="center"><blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Someone should go and invent an open standard and build a bunch of devices on it</p>&mdash; photomattmills (@photomattmills) <a href="https://twitter.com/photomattmills/status/910361827166638081">September 20, 2017</a></blockquote><script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script></div>

this reply of mine was kind of meant to be flippant, but it really got me thinking, what would it take to make a truly open IoT platform? What does that look like?

So first, and this is a thing [Matt](http://interconnected.org/home/2017/08/16/smart_home) said as well: it needs to work without the internet. Manual controls, default modes, all need to be part and parcel of the thing. Like smartwatches: most of them don't gracefully fail to 'just a watch' when you first have them and haven't set them up, they just fail completely to do anything. Smart bulbs are another example: If I spend $60 on a smart bulb, it better turn on and respond to a fucking dimmer out of the box without an app. It's not too much to ask; I know this because I've designed lightbulbs before.

So: let's say you have the OpenHome app (terrible name, we'll have to iterate on that), and you buy a light bulb that supports it. What does that setup look like? Ideally, you plug in the bulb, it turns on a bluetooth 4.0 radio and announces it's there to the world; your app sees it and tells you there's a new device, would you like to pair?

So, first: the device must work under all circumstances the dumb device worked. Second, service discovery and connection needs to be fairly seamless. once that's done, the device needs to advertise what sensors and services it offers. If only we had an API for dynamically building APIs lying around... oh yeah, [GraphQL](http://graphql.org/).

So the first thing you query for is a list of supported things to adjust and sense, and make a UI that doesn't suck for things like adjusting temperature and color and volume; and then just enable the sliders (come on, we know it'll be some sliders) that the service supports. For our hypothetical light bulb, it could be on/off (boolean), brightness percentage (interger out of 100), and maybe color (RGB hex, so an INT). Our hypothetical app has default and customizable, sharable setups for all of these values. You also need to be able to group devices (turn off all the lightbulbs etc).

Ideally you'd have a little wall-wart server (remember those? what a joke in these days of raspberry pis and [vocores](http://vocore.io/) &c) that you plugged in and actually all the new smart devices talked through it, so when you wanted to add a control device (tablet, phone, friend house sitting) it just joins the wifi, open the OpenHome app, it detects the OpenHome server (couple ways to do this), it asks you if you want to control all the things, and pings authorized users for ackles. Then, the same service discovery mechanism that works for one device will load the whole home into the newly minted authorized user's device.

Will anybody implement this? Probably not.
<span style="display:block;" class="center">
</span>
