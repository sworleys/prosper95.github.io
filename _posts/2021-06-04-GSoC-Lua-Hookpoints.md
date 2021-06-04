---
layout: post
title:  "Google Summer of Code 2021 - Lua Hook Points"
date:   2021-06-04 00:00:00 -0000
author: "sworley"
categories: dev
---

[FRR](https://summerofcode.withgoogle.com/organizations/4871589453103104/) 
got accepted again to Google Summer of Code for 2021 summer and we will be
working with a student to add a scripting system to FRR.

If you aren't familiar with GSoC take a look [here](https://en.wikipedia.org/wiki/Google_Summer_of_Code).

Basically, I will be mentoring a university student and guiding them as they work
through the project over the summer along with another FRR maintainer.

Okay so now the cool stuff. WTF are Lua hookpoints??? Well the project is [here](https://frrouting.github.io/frr-gsoc/year-2021/projects/lua-hook-points)
but the simplest way to explain it is with games. Are you familiar with modding 
systems?

Yea?

Okay well it's that... but ...

Basically the way a game engine lets you mod the game during runtime is through
a scripting system the developers added. This scripting system lets you hook into
game objects and subsystems with your own userdefined scripts/settings. It's
the exact same thing but with network objects and routing subsystems.

Lua is a great way to do this with C. Well, it's basically the goto scripting
language for C and actually a lot of game engines use exactly it.

Why is this cool for a routing stack? Well for one, we don't know any that have
anything like this! So there is a TON of ideas for things we could do.


Like imagine only advertising certain BGP routes if the weather is sunny and
others if it's clear. Yea you can do shit like that with a Lua hook in a BGP
advertise routemap.

Or maybe you only want to install /32 routes into the kernel if it's a Tuesday.

Or you have some database constantly being populated with whitelist nexthops and
you want to use these without having to reconfigure FRR all the time. Write a Lua
script to query it and change your routes before install.


Nuts right?
