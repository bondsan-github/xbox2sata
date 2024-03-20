Aim
===
Create a IDE to SATA bridge PCB with pass-through socket for XBox DVD cable. 

Sources
=======
- https://www.psdevwiki.com/ps3/88SA8040-TBC1
- https://www.ioi.com.tw/products/proddetail.aspx?CatID=101&HostID=2010&DeviceID=3002&ProdID=1010114
- https://en.wikipedia.org/wiki/Parallel_ATA
- https://www.startech.com/en-gb/hdd/ide2sat2

Completed
=========
Unverified schematic of Startech IDE2SATA pcb

To do
=====
Measure components;
- L1
- R5
- R6

- Find suitable 5V and ground points to tap on XBox motherboard.
- Measure available space inside XBox under DVD drive.

- Can xbox ide connection be directly connected to DVD connection?
  - Simular how a IDE cable does?
  - IDE cable does have CSEL tied hi or low depending on device?
- Can LED circuit be removed? Is it for HDD activity?
- CSEL cable selection can be fixed as DVD will always be device 0 (slave) and SATA device 1 (master)?
- What capacitors are required for power input from xbox motherboard?

Requirements
============
- 5V and ground from xbox motherboard
- xbox IDE connection
- DVD IDE connection
- SATA connection
- Marvell 88SA8052 IC
  - Crystal oscillator
  - 1V2 for Vdd
  - 3V3 for Vddio and pull-ups
    - power conditioning?
  - CNFG0,1,2 setup
  - T0,1,2,3,4,5,6,7,8 setup

Desirables
==========
Marvell 88SA8052 datasheet

Software used
=============
- Proteus 8.15 SP1
- GIMP 2.99.18 development release 
