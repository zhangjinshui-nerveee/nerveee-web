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
### How to transfer parameters from MATLAB command to Simulink?
- Save the data in .mat file, and read it in simulink.
> Be careful. When saving data to xxx.mat file, you need to use `append` mode. Otherwise, you would lose all data in the mat file already. 
```
save 'xxx.mat' var '-append'
```

## FFT Code
After get the signal (structure with time), perform the following code. 
'''
Ts = 1e-8
Fs = 1 / Ts
t_end = 1e-5
t = linspace(0, t_end, t_end / Ts)
f1 = 100e3
a1 = 1
f2 = 300e3
a2 = .2
f3 = 700e3
a3 = .5

X = a1*sin(2*pi*f1*t) + a2*sin(2*pi*f2*t) + a3*sin(2*pi*f3*t)
plot(t, y)
Y = fft(X)
L = length(X)
P2 = abs(Y/L)
P1 = P2(1:L/2+1)
P1(2:end-1) = 2*P1(2:end-1);
f = Fs*(0:(L/2))/L;
semilogx(f,P1, 'ro') 
'''
The above is a test with a mixture of different frequency sinusoidal signals. 





## Auto running and saving

