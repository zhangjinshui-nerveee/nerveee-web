---
title: Notes on MATLAB / Simulink Use
date: 2022-02-16 07:25:00
tags:
- Power Electronics
- MATLAB
category:
- Power Electronics
---

# Simulation Script of Simulink

Usually we need to run the simulation multiple times before the problem is solved or found. When it takes long time, we don't want to stay in front of the computer and do nothing. <br>
Actually, we could run the simulation by script. Realize the automation of simulation. <br>
Also, we could run calculations in MATLAB environment and analyze the simulation results after. 

Here, we are going to run a power electronics model for several times, and after each simulation, do FFT analysis on the out voltage waveform. The data would be saved in a matrix. 

## Simulation Command
[Run simulation programmatically](https://www.mathworks.com/help/simulink/ug/using-the-sim-command.html)

But first, you need to make the parameters in simulink accessible to MATLAB. 

## FFT Code


## Auto running and saving

