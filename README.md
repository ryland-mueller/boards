# TTPMS V2 Board Hardware Description & Configuration Files
TTPMS V2 [custom board definitions for the Zephyr RTOS](https://docs.zephyrproject.org/latest/develop/application/index.html#custom-board-devicetree-and-soc-definitions "Zephyr RTOS Documentation"). These files are required in order to build and flash a TTPMS V2 board.

Each board definition represents a specific set of PCB design files, and in most cases a specific physical PCB assembly (with exceptions as noted below).

For example, `ttpms_is_2_0` is the first design of the TTPMS V2 internal sensor main board.

As another example, `ttpms_rx_2_1` will be the first revision of the TTPMS V2 receiver hardware, which will bring out GPIO pins to the RBG status LED drivers.

The odd case is `ttpms_exm_2_0`, the common external sensor main board which is used for both front tire and rear tire varieties of external sensors. Since the forward face of the front tires move significantly throughout the range of steering, a larger IR array/camera is required to capture this area, which requires a higher supply voltage, and in turn a different voltage regulator to be populated on the physical PCB. So although there are actually two different physical main board assemblies, and two different daughter boards to mount the IR arrays, these differences in hardware are not relevant to the information contained in the board definition, so both varieties can be represented by the same `ttpms_exm_2_0` definition files.

If future revisions of physical PCBs do not modify the information contained in the board definition files (mostly pin mapping), a new board definition will not be created. For example, a theoretical revision 1 of the internal sensor main board with only a new battery connector would still use the existing `ttpms_is_2_0` board definition, even though it would physically be tagged "TTPMS V2.1".

## Overview of the TTPMS project:<br />
*link coming soon*<br />
<br />

## All the TTPMS repos:
### TTPMS V2 (third-generation)
**Receiver Application:** https://github.com/ryland-mueller/ttpms_v2_receiver<br />
**Internal Sensor Application:** https://github.com/ryland-mueller/ttpms_v2_internal<br />
**External Front Sensor Application:** https://github.com/ryland-mueller/ttpms_v2_external_front<br />
**External Rear Sensor Application:** *coming soon*<br />
**Board Definition Files:** *This Repo*
### TTPMS (second-generation)
https://github.com/ryland-mueller/ttpms<br />
### TTPMS (first-generation)
https://github.com/lukegarland/ttpms<br />
