# Bypassing the PSLab's Resettable Fuse

The PSLab features a __resettable fuse__, designed to protect its sensitive parts from overcurrent.

![PSLab drawing with relevant parts highlighted](pslab_drawing.png 'Figure 1')

<span style="color:#D81B60">Cerise</span>: Resettable fuse
<span style="color:#1E88E5">Blue</span>: Battery charge indicator LEDs
<span style="color:#FFC107">Yellow</span>: STATUS LED
<span style="color:#004D40">Dark cyan</span>: +5V and GND pins

In some cases, the fuse may incorrectly cut power to the PSLab during startup. The symptoms of this are:

- The PSLab does not boot, i.e. the __STATUS LED__ does not light up.
- The __battery charge indicator LEDs__ flash irregularly.
- The PSLab emits a high-pitched noise.

If at least two of these symptoms are present, try bypassing the resettable fuse to resolve the problem. Once the fuse has been bypassed and the boot process has completed, the problem does not reoccur.

To bypass the fuse, use one of the following methods.

## Fuse bypass method 1 - Power via +5V line

The PSLab can be powered by supplying 5 V between the pins labelled __+5V__ and __GND__. Suitable sources of 5 V include:

- Programmable voltage sources, a common laboratory equipment.
- A fixed 5 V power supply, such as the power supply of a Raspberry Pi.
- Three _fresh_ alkaline cells connected in series.

The supply voltage much exceed 4.5 V in order for the PSLab to be able to boot. Three alkaline cells just barely achieve this voltage when they are fully charged; if they are used, or have been sitting in a drawer for some time, they may not be able to supply sufficient voltage.

__Be careful not to overvolt the PSLab! Supplying a voltage above 5.5 V on the +5V pin may permanently damage the device!__

![PSLab powered by three alkaline cells](alkaline.jpg 'Figure 2')

## Fuse bypass method 2 - Short circuit fuse

The fuse can be short circuited by connecting its two terminals using e.g. a jumper wire or a metal paper clip. This must be done while the device is powered via USB.

![Resettable fuse short circuited by jumper wire](short.jpg 'Figure 3')

__Be careful not to touch any other part of the PSLab with the jumper wire! Doing so may permanently damage the device!__
