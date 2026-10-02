---
title: "USB Hub"
author: "Anirban185"
description: "Click me to edit the description of your project."
created_at: "2026-10-02"
---

# 2026-10-02: CAD Devlopment

**Total time spent: 1.5 hours**

So today's task is to make the enclosure for the USB hub. I am fairly new to CAD, so it was not gonna be a smooth session. I got started by creating a 65.6 by 45.6 base, then I added stumps for the PCB to sit on, and I extruded stumps on the stumps to keep the PCB position correct. That took some time because I couldn't get the circles in the place the PCB is gonna sit, since I was measuring from the side, but then I realized the PCB is 60 by 40 and my base is 65 by 45, which was a silly mistake. After I got that sorted out, I made the walls — first a wall 4.3mm tall, with 2.5mm to compensate for the stumps the PCB will be standing on, and 1.8mm so the wall reaches near the bottom of the USB ports. Then I extruded the wall, exempting the spots where the USB ports will be, and kept the cutouts for the USB ports open from the top, since the lid is gonna fill those areas.![image](https://cdn.hackclub.com/019fcf08-dddf-7d10-83a0-4e599ff0236b/Screenshot_2026-08-04_20-55-56.png)
For the lid, I started with the same 65.6 by 45.6 base, then added skirts and rounded them, and made cutouts for the USB ports so the ports don't obstruct the skirts. Then I made tabs extruded from the base that are gonna fill the open tops of the cutouts on the main enclosure.![image](https://cdn.hackclub.com/019fcf19-d17d-76b0-98bf-45dd42431914/Screenshot_2026-08-05_04-54-50.png)
I know I didn't add any spots for screws or a locking mechanism to hold the lid — that's because I didn't see big enough areas for M2 brass inserts, and snap-on mechanisms aren't as reliable, so I'm thinking of using some kind of glue that I'd be able to heat and pry off if needed in the future.
For the assembly, I inserted the enclosure parts and PCB, first mating the PCB into the enclosure base, then mating the lid to the base, and after tweaking the offset a little, the assembly was done too.
![image](https://cdn.hackclub.com/019fcf0a-4639-76a8-93ad-24a972c5b649/Screenshot_2026-08-04_20-58-21.png)

# 2026-10-02: Schematic and PCB designing

**Total time spent: 4.0 hours**

I read the schematic part of the provided guide, and I think I am gonna improvise a little instead of following it straight. So the plan is I am gonna have 2 upstream ports instead of 1, using a power and data mux. After reading a lot of datasheets and comparing parts, I have selected TS3USB221 as the Data mux and TPS2113A as the power mux. Also, I am also adding an AMS1117 voltage regulator for 3.3V for the TS3USB221 data mux. I mostly followed the guide for the SL2.1S Chip part and decided to use 4 USB-A ports as the downstream ports. And that was it for the schematics part. 
![image](https://cdn.hackclub.com/019fc75b-5da1-7d1d-a143-4ff0619a977d/SCH_Schematic1_1-P1_2026-08-03.png)
After a break, I converted the schematic to the PCB, and looking at this, this is gonna be much more complex than the circuit in the guide. So I got started and placed the components in their places. First, I am placing the USB ports; I decided to place the upstream ports on opposite sides on the short side of the rectangle(the PCB is a 60 by 40 mm rectangle) and the downstream ports on the long side of the rectangle. I placed the ICs in the middle of the long side, placed the small components (e.g., capacitors) near their main components, and after that was done, I placed the AMS1117 on the bottom side. Now it’s time for routing; first, I am routing the passive components as the guide suggests. Then I routed the data lines and 5V rails, then everything else that was left except the GND, cause i am gonna make a ground plane on the top. After a few tweaks, the ground plane on the top was ready. After inspecting it, I moved to making a ground plane on the bottom side too. At the end, I decided to add some jokes using silkscreen to add some character. And just like that, the PCB is done.
![image](https://cdn.hackclub.com/019fc75c-a29d-7856-abd7-5550015c3e58/PCB_PCB1_2026-08-03.png)
![image](https://cdn.hackclub.com/019fc75e-0058-7c1d-9b1f-86f7e693e812/PCB_PCB1_2026-08-03%20(1).png)

