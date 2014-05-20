![cuwo](http://mp2.dk/cuwo/logo.png)
====

cuwo is an open server implementation for Cube World, written in Python and
C++. It currently has the best protocol coverage among all the server projects
out there, and has features like

* Cross-platform support (Windows, Mac OS X, Linux, FreeBSD, what have you)
* File/console logging
* MOTD message
* Scripting (see the minimal welcome.py example)
* Advanced configuration
* Ban system
* Commands (/kick, /say, /whereis, /setclock, /kill, /stun. etc.)
* Rights management (/login password)
* IRC bot
* PvP script
* DDoS prevention
* Lower CPU requirements than normal server
* Optimizations in C++
* Master server on http://cuwo.org
* Support for 40+ players
* ... and much more!

Running
=======

On Windows, see the
[quick-start guide](https://github.com/matpow2/cuwo/wiki/Quickstart) for a
quick way to get started.

On Linux/Mac OS X/FreeBSD/etc., make sure you have Python >= 3.3 and
Cython installed on your machine, along with native compilers.
On Python versions below 3.4, you will also need asyncio installed.

To build cuwo, run `python setup.py build_ext --inplace`.
To run the server, run `python -m cuwo.server`.

Optionally, install the irc3 package to enable IRC bot support.

Status
======

In terms of the protocol and features, the following has been implemented:
* Player join/leave
* Player movement and animations
* Magic/arrows/etc. relay
* Player hits on entities/other players
* Item pickup/drop
* Time management
* Terrain generator

A lot is still to be implemented gameplay-wise. Most importantly, NPCs and mobs
have not been implemented yet. The terrain generator is completely working now,
but work still needs to be put into creating intelligent AI and proper
behaviour.

Also, interactive objects (like doors, beds), have not been implemented
yet, but with the terrain generator, it should be a fairly simple feature.

Other features include
* MITM proxy (for reverse-engineering)
* Cube World/Qubicle model converter (tools/convertqmo.py)
* Map viewer (tools/mapviewer.py)

FAQ
===

* **Q.** How do I pronounce 'cuwo'?

* **A.** 'coo-woo' (no, not 'kew-woh')

* **Q.** I am not a programmer, and I can't reverse-engineer anything. How do
         I help?

* **A.** We need people who can create end-user documentation as well! Have a
         look around, and see if anything is missing on the wiki.

* **Q.** What is a MITM proxy?

* **A.** A MITM proxy sits between your client and server, and can manipulate
         and inject packets. It's not really useful to the normal user, so
         use the regular cuwo server instead.

* **Q.** Can I donate to the project somehow?

* **A.** Yes! You don't have to, of course, but it will help bring
         the server forward.

* [![Click here to lend your support to cuwo and make a donation at pledgie.com!](http://pledgie.com/campaigns/24724.png?skin_name=chrome)](http://pledgie.com/campaigns/24724)

Special thanks
==============

Sarcen - help with protocol variables, scripting, anticheat

Perl - protocol RE

ZeZeene - web interface for master server

Lord_Nightmare - terraingen help and support with x86

Kyle - master server JS

MazeXD - master server JS and design

cs475x - website design

Kainzo - testing

uwee - protocol variables

Somer - help with some protocol variables

Favorlock - scripting and commands

SLoW - scripting

DRayX - encrypt.py and protocol RE

MAT4DOR - cub model details

Xaymar - RE and character details
