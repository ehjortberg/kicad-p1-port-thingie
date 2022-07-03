# P1 Port Thingie
This is a small board to bridge the P1 port of the Swedish electricity meters with Home Assistant.
The level conversion part of the schematics is based on the examples on the [software](https://github.com/psvanstrom/esphome-p1reader) github page.
The rest is basically a 5v to 3.3V LDO and ESP07 required components.

It can be programmed with esphome using a 3.3V ftdi cable or similar. External power via rj12 is probably needed as the ftdi cables usually do not have enough power on 3.3V
Installation guide and software: [https://github.com/psvanstrom/esphome-p1reader](https://github.com/psvanstrom/esphome-p1reader).

Edit the p1reader.yaml and set board: esp01_1m

There is sometimes interference on the RX line when programming so it's preferable to program before adding the transistor.

A box can be 3D Printed. [Download .stl files](https://www.thingiverse.com/thing:5337456)

![top side](images/p1-port-thingie-top.jpg)
![bottom side](images/p1-port-thingie-bottom.jpg)
![photo](images/p1-port-thingie-photo.jpg)


# BOM

| Reference | Value | Footprint |
| --------- | ----- | --------- |
|Button1||Button_Switch_SMD:SW_SPST_TL3342|
|Button2||Button_Switch_SMD:SW_SPST_TL3342|
|C1|100nF|Capacitor_Tantalum_SMD:CP_EIA-6032-15_Kemet-U_Pad2.25x2.35mm_HandSolder|
|C2|100nF|Capacitor_Tantalum_SMD:CP_EIA-6032-15_Kemet-U_Pad2.25x2.35mm_HandSolder|
|JP1 Connector|6P6C|Connector_RJ:RJ12_Amphenol_54601|
|Q1|BC817W.115|Package_TO_SOT_SMD:SOT-323_SC-70|
|R1|4K7|Resistor_SMD:R_0805_2012Metric_Pad1.20x1.40mm_HandSolder|
|R2,R3,R4,R5,R6,R7|10K|Resistor_SMD:R_0805_2012Metric_Pad1.20x1.40mm_HandSolder|
|U1|LD1117S33CTR|Package_TO_SOT_SMD:SOT-223-3_TabPin2|
|ESP07|||
