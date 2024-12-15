# SINCLAIR QL 512kB External Rom Expansion

**This board will provide up to 512kB aditional of static RAM (*fast-ram*) to the sinclair QL.**

Full documentation and wiki page under construction

---

![My image](images/schema.png)

---

![My image](images/RAM_Expansion_QL_Front.jpg) 

![My image](images/RAM_Expansion_QL_Back.jpg) 

---
**Boards work fine in the QL used for testing**

Two board can be stacked to got a maximun of 898Kb of Memory (*same as Miracle's Trump Card*).

Be aware **you can not have 2 memory expansion in same area** (*Jose Leandro's QBide, Trump Card, etc*).

Provide a expansion conector to allow conect aditional interfaces.

There area available 4 configuration trough switches in the PCB.
* 00 => 512kB - This is the standar 512kB expansion for any QL
* 01 => 256kB - This is for use as a second expansion, use the full QL space for a maximun of 898kB, be aware that this is incompatible with a lot of expansion card, so use with caution (Any expansion card that do not use jumper/switch for configuration will be incompatible).
* 10 => 192kB - Similar to 256kB provide aditional space for expansion cards correctly configured.
* 11 => 128kB - Similar to 256kB provide aditional space for expansion cards correctly configured.

Be aware that **the configuration of 128Kb can not be installed alone**.
For be able to use 128kB, for a total of 768kB, is mandatory to have an aditional expansion card that put ROM in address E00000h, in other case the QL ROM will hang indicating RAM malfunction, because a weired overlap of the internal 128kB with this external 128kB.

---
## GERBER FILE

Gerbers ready to use.

[Click here to download the Gerber](Gerber/Gerber_Popopo_QL_RAM_Expansion_v1a.zip) 

---

https://www.instagram.com/p/CZWfWcUM5mx/

In the GAL folder there is the source code to be compiled with GALasm that you can found here: https://github.com/daveho/GALasm

## Mini Trump Card Compatibility

Alvaro Alea has done a version of the trump card disk interface here: https://github.com/alvaroalea/QL_MiniTrump3 , this interface do not provide memory like the original one. You can combine two of this card and the minitrump to got the same of the original trump card.

You should conect the 512Kb Card to the QL, the MiniTrump Card to the 512Kb, and the +256Kb card to the Mini Trump, and in this board you need to change Switch (*SW1*) to 2-3 to allow the Minitrump card to coordinate with the second memory card.

![My image](images/QL512K_RAM_Expansion_Front_Full.png) 

![My image](images/QL512K_RAM_Expansion_Front_raw.png) 

![My image](images/QL512K_RAM_Expansion_Back.png)



## Credits & License
Original project of (C) 2022 Alvaro Alea Fernandez, who based his development on the work of McLeod Ideafix, Jose Leandro, Zerover and tcat among others. 

Thanks to Alberto Benítez (Lince) for his support in improvements the signals.

License under: CERN Open Hardware Licence Version 2 - Strongly Reciprocal

https://ohwr.org/cern_ohl_s_v2.txt

