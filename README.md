# Shield Board for Arduino-Uno
This repository is a work on designing a PCB for a Shield Board that sits atop an Arduino Uno board. The design of schematics and PCB Layout is done on Altium Designer v25.8 platform. This work is referred from a course available at [Altium Education](https://education.altium.com/).

## The PCB
The designed Shield Board utilises a power regulator designed by [Texas Instruments' WeBench](https://webench.ti.com/power-designer/). The Power Design is a DC/DC, with Input Voltage set at 12V, giving an Output Voltage of 5V at 1A. The Power regulator chosen is a balanced **TPS562200DDCR** IC. There also is a bank of 2 LED components. The schematic is designed from components mentioned in TI's Bill of Materials(BOM) in the designer's webpage.

It is to note that certain components mentioned in the BOM are not available in Altium Designer. The solution is to download their ECAD models from distributors like Arrow Electronics, Digikey, or Mouser Electronics. The component symbols and footprints can also be found at UltraLibrarian. 

## Functional Requirements
1. Receive power from a 12V DC input
2. Regulate power down to 5V DC
3. Deliver 12V DC to a bank of 2 LED lights in parallel
4. Provide 5V DC power to main Arduino Uno board
5. Provide enough current to power Arduino and LEDs
6. Regulate power with atleast 90% efficiency
7. LEDs are SMD(Surface Mount Device) parts with high power output (10W)
8. Components placed only on top layer
9. Total board thickness approximates to 62mils

## Components
The LEDs selected for this board is the part number MKRAWT-00-0000-0D0H235H. It is found from its datasheet that it uses 1A current when powered at 12V DC.
![Current v. Voltage](https://uploads.teachablecdn.com/attachments/IoXiZBL8Rtq5SeEAdqOI_Untitled.png).
Other parts can be found from Manufacturer Parts Search in Altium Designer. IF not present, they can be looked up at their distributors' webpage. Further, a table is shared below to opt for alternatives to missing parts:
| Part Number | Description | Alternate Part Number |
| ------------ | ---------- | --------------------- |
| RC0201FR-0710KL | 10kOhm resistor, 0201 package | ERJ2RKF1002X |
| RC0201FR-0756K2L | 56.2 kOhm resistor, 0201 package | CRCW020156K2FNED |
| VLP8040T-3R3N	| 3.3 uH inductor | NRS8030T3R3MJGJ |


