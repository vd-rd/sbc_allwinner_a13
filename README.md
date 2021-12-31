## Description
TBD


### Features

 * CPU - Allwinner A13 (ARM Cortex-A8 @ 1Ghz)
 * RAM - DDR3 512MB max (8Gbit module)
 * microSD card slot
 * microUSB OTG interface
 * standard ApolloIoT expansion header
 * LCD connector
 * WIFI/BT via RTL8188cus module


### Power considerations

A13 features a few power rails:
* VDD-CPU - TBD - from AXP209
* VDD-INT - 1.2V - from DCDC
* VDD-GPIO - 3V3 - from AXP209
* VDD-DRAM - 1V5 - from DCDC
* AVCC - 3V - from AXP209

The datasheet states that AVCC and VDD-DRAM must be present at all times (even standby).
VDD-INT and VDD-CPU can't be tied together because VDD-CPU is DVS enabled.


### Memory considerations

A13 DRAM controller doesn't provide DDR-CS. On the memory side the pin is tied to GND.
Memory tuning should be performed as [described here](sunxi_link)


### Resources

You can find all necesary information to build or evaluate the module here:
   - [Fabrication files](https://github.com/vd-rd/sbc_alw_a13/releases)

Inspiration for this has been drawn from:
* Olimex boards 
* Sunxi community
