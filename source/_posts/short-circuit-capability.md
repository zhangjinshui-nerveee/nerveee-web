---
title: Short Circuit Capability of Power Semiconductors
date: 2022-02-06 19:46:24
tags:
- Power Electronics
- Wide-Band-Gap
- EMC
category:
- Power Electronics
---

> The object here is mainly for 1200 V SiC MOSFET. To be more specific, Infineon [FF11MR12W1M1_B11](https://www.infineon.com/cms/en/product/power/mosfet/silicon-carbide/modules/ff11mr12w1m1_b11/). 

# Information collection

1. The SiC MOSFETs failed after short-circuit operations of 80 us and 50 us at 10V and lSV gate bias respectivel.[1]
> The test is under a 400 V DC bus. 
2. An interesting phenomenon has to be noted that the drain current at Vg = 10V increases at elevated temperature but it decrease with the temperature at Vg = 20V.[1]
> [1] gives a detailed info about SC under 400 V DC bus: when to fail, peak current (density). But how can we predict the short circuit performance under smaller voltage (like 10 V)? And will they fail then?
3. Literature mainly care about conditions under 400V+ bus. The SC capability is important because the SiC need to withstand till the system knows this is a short circuit and takes actions. 
> What we need here may need the simulation. Not the focus of publishment. 

# Simulation
- Model provided by Infineon is designed for PLECS thermal simulation. Dynamic performance (electrical) would not present. 
- In order to observe the dynamics, we need to add stray parameters manually.
 

# Definition of Short Circuit Capability
- Short-circuit capability is defined by the energy density applied to the device during the period of short-circuit withstand.


# References
[1] [Short-Circuit Capability of 1200V SiC MOSFET and JFET for Fault Protection](https://sci-hub.se/10.1109/APEC.2013.6520207)
