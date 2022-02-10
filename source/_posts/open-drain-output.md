---
title: Rail-to-Rail Input Comparator Debugging
date: 2022-02-09 20:41:29
tags:
- Power Electronics
---

# Output Type
Usually the product would have two different types of output: Push-Pull and Open-Drain. 
> In this case, we are using the chip from Microchip. MIC7211/MIC7221. 

Be careful that  7211 is push-pull output and 7221 is open-drain output. Therefore, if we use MIC7221, we need a pull-up resistor to the power supply. Otherwise there will NOT be any output (always 0). 

Meanwhile, when choosing pull-up resistor, we have to find the proper "Supply Current" in the datasheet, which is 7 uA under 5V Vdd. Therefore, the resistor should be about 700 kOhm. 

- Phenomenon of over supply current
If the resistor is too small, (say 10kOhm), therefore will be over-supply-current. Then the MOSFET will be turned on forever, it won't change with the input until you shut the power and restart the board. 
