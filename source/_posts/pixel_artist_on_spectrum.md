---
title: Pixel Art on Magnetic Spectrum
# date: 2024-09-22 07:07:07
---

# Background
This idea traces back to a cross-displin biomedical engineering project that I was working on from 2022 to 2024. The core of this project is magnetogenetics. In principle, **magnetogenetics** is to synthesize nanoparticles that can be selectively heated by magnetic field of different frequencies. 
Say, nanoparticle A can only be heated by 50 kHz wave but cannot by any other. 
While particle B can only be heated by 500 kHz but not any other. 

More explanation can be found in these papers:
1. [Subsecond multichannel magnetic control of select neural circuits in freely moving flies](https://www.nature.com/articles/s41563-022-01281-7)
2. [A wireless millimetric magnetoelectric implant for the endovascular stimulation of peripheral nerves](https://www.nature.com/articles/s41551-022-00873-7)

My role here is to build a prototype that can generate these magnetic waves at the same time. The intensity shall be beyond 80 mT, which is quite a lot. 

You professionals may think that okay, this job can be easily done with some simple resonant circuit. Unfortunately, the frequency is not fixed and we may need to change it from time to time, ranging from DC to 5 MHz. Resonant circuits cause us trouble since they can't change their frequency freely without changing the hardware.

Then, we decided to build a ultra-fast modular multilevel circuit (MMC). MMC is normal in grid / motor drive applications. There haven't been any one that can provide a high power with a 5 MHz output bandwidth, unitl now. 

Even though it sounds unbelievable to operate a clumsy power grid inverter at 5 MHz, MMC, the technology itself, is indeed capable of doing so. The details of implementing this idea can be found in this TIE paper. 

Insert reference here. 

Of course, I wrote this paper. 

# Waterfall Presentation

Initially I was using the specgram / spectrum / waterfall diagram to check if the output frequency aligns with my expectation. 
Professionals, yes I know what you may think. A Fourier transform graph would do the job. 

Yes, indeed, if the output profile requires only one configuration. In our study, we want to show off a bit more. We want to dynamically heat different nanoparticles. For example, heat the 50 kHz channel for 10 milliseconds and heat 500 KHz for another 10 milliseconds. Try to replace the above numbers with any other random number, and that's the challenge I was facing. 

Therefore, I need a waterfall diagram, whose x-axis is time, y-axis is frequency, and color of every pixel reflects the intensity of the magnetic field intensity. 

Things work pretty well. 

Insert channel mixing figure. 

# Spice Things Up
I was looking at the waterfall diagram. And then I realized that this prototype can do way more than just this. We can basically contol the spectrum distribution of every moment. Why not spice things up a little bit?

And here we are. 

Insert Arecibo message.  

Explain it. 

# Results
