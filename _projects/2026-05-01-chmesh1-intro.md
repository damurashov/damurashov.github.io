---
layout: post
title: CH Mesh 1: Intro
tags:
- Project CH Mesh
---

# What is this projects about

- an attempt to develop an alternative solution to meshtastic devices, usually built on ESP32, or nRF52
- port the meshtastic stack on the device
- make it compatible w/ the meshtastic application
- probably, make an alternative meshcore firmware

Usefulness. Why doing something like that

- no real economical reasons. Just want to poke into this Chinese phenomenon. It's cool
	- i can see to what extent I can reproduce whatever lilygo, or heltec have done, but with this little stone.
- if you have some practical objectives, just use ESP32. If all you need is connectivity, there's nothing better. It's tried, and through, it's dirt-cheap, it's powerful, it's efficient because you can offload something to the low power co-processor if you need to, it arguably has the greatest community ever, and the software support is outstanding. Thus far, it's the best

Why v208

- cheap chinese micro, but 128K flash, 64K RAM, Ethernet PHY (10Mb though), BLE, USB
- cheaper than ESP.
	- Hopefully (TODO DM validate that, see current consumption, and voltage), more efficient. That's a non-goal anyway

# Relevant links

- wch32 reference
- wlink
- minichlink
- mounriver studio
	- do you trust some obscure closed-source IDE from China to run bare-metal on your machine?
- debugger
- the toolchain

# Gettingstarted

- getting the debugger
- building minichlink, and wlink
- exporting CMake project from MounRiver studio
	- greatest kudos to them for the HAL, and for the out-of-the-box experience
- building from example
- exporting the cmake project
- configuring the debugger
	- attach vscode configuration too
- running the example
- examining the example, and the reference manual
	- no description to the radio part (AFAIK, same thing w/ ESP?)
	- everything about configuring the hardware is in `.a` file. Have no interest into reverse engineering it yet;
- poking into meshtastic firmware
	- wtf is GATT
	- getting the bits I need
	- nanopb

# Sides

- reversing the BLE .a lib