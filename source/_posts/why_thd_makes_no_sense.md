---
title: Why THD makes no sense and we need THD+N
date: 2022-02-11 15:38:15
tags:
- Power Electronics
---
# Total Harmonics Distortion (THD)


# Total Harmonics Distortion and Noise (THD+N)

# How to measure THD and THD+N
In simulink, the Power GUI has a build-in tool "FFT Analysis". We can rely on this tool to perform FFT analysis and furtherly the THD or THD+N. 

- If we need to perform FFT analysis on certain signals, we need to save them to workspace while simulating, the format should be structure with time. 
- And remember to deselect the option in the "model setting" --> "Data Import / Export" --> "Single Simulation Ouput". 
- Otherwise, all the "to workspace" data would be bunched together in a simulationOutput variable and the FFT tool cannot recognize the signals we saved and we need to split them manually. 
- Deselect this option, you can see the output variable in the MATLAB workspace after simulation, and its format is "struct" instead of "SimulationOutput". 

# SINAD (Signal-to-Noise-and-Distortion-Ratio)

# References
[1] [Understand SINAD, ENOB, SNR, THD, THD + N, and SFDR so You Don't Get Lost in the Noise Floor](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&ved=2ahUKEwiij8T3-qf2AhUpWN8KHT_HBLwQFnoECEYQAQ&url=https%3A%2F%2Fwww.analog.com%2Fmedia%2Fen%2Ftraining-seminars%2Ftutorials%2FMT-003.pdf&usg=AOvVaw1bzXTzeZEuceHXPY9U21On)
