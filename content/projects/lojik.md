---
title: Lojik
description: A bunch of logical operators as well as some excellent new sequencer primitives
author: tomf
compatibility: { v05: false, v06: true }
contact: https://forum.orthogonaldevices.com/u/tomf/summary
link: https://github.com/tmfset/er-301-custom-units
latest version: v0.4.0
files:
  - lojik-0.1.1.pkg
  - lojik-0.2.0.pkg
  - lojik-0.4.0.pkg
units:
  - { name: And, category: Gates }
  - { name: DLatch, category: Gates }
  - { name: Latch, category: Gates }
  - { name: Not, category: Gates }
  - { name: Or, category: Gates }
  - { name: Pick, category: Gates }
  - { name: Register, category: Sequencers }
  - { name: Seq, category: Sequencers }
  - { name: Trig, category: Gates }
  - { name: Turing, category: Sequencers }
  - { name: Wait, category: Gates }
---

Hello all let me introduce Lojik! A collection of bespoke units for the latest v0.6 firmware, using the amazing, newly available, DSP layer. This collection includes a bunch of logical operators as well as some excellent new sequencer primitives.

These units all perform as well as the built-in core units, using < 1-2% CPU each.

## Gates

- Trig - Is the input signal greater than zero?
- Not - Is the input signal less than or equal to zero?
- And - Is the left and right input greater than zero?
- Or - Is the left or right input greater than zero?
- Pick - Output left on gate low, right on gate high.
- Wait - Basically a clock divider.
- Latch - An SR latch, set it high and reset it low.
- DLatch - A data latch, essentially just a sample and hold.

## Sequencers

- Register - A shift register that can hold up to 64 steps of arbitrary voltages. Contains a built in random source to sample from.
  <md-img src="lojik/lojik__000.png" alt=""></md-img>
- Turing - Basically just a register with a scale quantizer in front of it, ideal for quickly generating V/Oct sequences.
  <md-img src="lojik/lojik__001.png" alt=""></md-img>
- Seq - A step sequencer
  <md-img src="lojik/lojik__002.png" alt=""></md-img>
