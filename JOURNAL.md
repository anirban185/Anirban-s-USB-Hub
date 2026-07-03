# 3/7/2026 21:52 - Schematic Designing

Time Spent: 1.67 Hours

So today's task was making the schematic. First, I followed the guide and made the circuit step by step. It took more time than expected because this was my first time using EasyEDA. I normally use KiCad, but I used EasyEDA today because the guide used it, and I figured it would be easier to follow along in the same editor. 

So I made a hub with a Type-C upstream and 4 USB-A downstream ports. After the base schematic from the guide was done, I went in and made some of my own changes and added features. First, I added some bulk capacitors to help with current spikes. Then I added a TPS2113A Power MUX IC, a TS3USB221 Data MUX IC, and a USB-A plug, making a USB hub with 2 upstream plugs that automatically pick whichever plug is connected. And that was it for today.

![image](https://cdn.hackclub.com/019f28c9-c8f3-7abd-8fbe-4cb552bfd26d/SCH_Schematic1_1-P1_2026-07-03.png)
