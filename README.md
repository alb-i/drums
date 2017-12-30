# drums
A jack-audio X-platform drum sampler hacked together in D


Quality Disclaimer
==================

This repository contains code that I hacked together in order to generate
play-along metal drum tracks. I started the project in 2015 and got it working
for me by early 2016; but I wasn't satisfied with the overall code quality, so
I wanted to fix this before I release the software. Well, I didn't fix anything
and I will probably never have enough time to do so, therefore I am releasing
this steaming mess of code.

About
=====

The program *drums* is a proof of concept that you can write non-trivial audio
applications in D, and that you can end up with software that runs on
  - Windows via cygwin
  - MacOSX
  - Debian Linux

What does *drums* do?
=====================

Drums is a program that listens for MIDI input and plays back a bunch of
samples accordingly. It has a primitive GUI that can be used to test
the setup of the sampler without having to connect it to

What does *synthesize* do?
==========================
Synthesize is similar to a modular tracker or sequencer,
you can compose and cobble together different drum patterns
which on playback will generate MIDI events that drive the sampler.
There are two modes, one for hackers, and one called *./sketch.sh*
with a more decent GUI -- use this one.
A nice feature here is the rehearsal mode that allows you to display
your guitar tabs in a riff-wise fashion; so you don't have to manually
switch pages anymore.

Mileage May Vary
================

In general, I made several not so good choices. First, I used dlangui,
which is pre-1.0.0 software and therefore breaks rather often.
The current version from github (dlangui 0.9.173+commit.8.g24d70c0e:)
seems to work fine, though.

There is also a port of libjack available via dub, unfortunately there were
some issues with it, so I
had to hack it, and the software won't work with the official version.
