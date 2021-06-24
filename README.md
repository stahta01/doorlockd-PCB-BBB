# doorlockd-PCB-BBB

Kicad drawing for doorlockd electronics on a Beagleboard black cape.
<img src="https://raw.githubusercontent.com/wie-niet/doorlockd-PCB-BBB/master/preview-rev0.02.png" alt="Preview doorlockd-PCB-BBB Rev0.02">

[<img src="https://raw.githubusercontent.com/wie-niet/doorlockd-PCB-BBB/master/schematic-rev0.02.png" alt="Schema doorlockd-PCB-BBB Rev0.02">](https://github.com/wie-niet/doorlockd-PCB-BBB/blob/master/schematic-rev0.02.pdf)




### component list
|Ref| |Value|
| --- | --- | --- |
|C1|C|1uF |
|C2|C|1uF|
|C3|CP|470u|
|D1|LED|LED|
|D2|1N4007|1N4007|
|D3|LED|LED|
|D4|1N4007|1N4007|
|J1|Conn_01x02|LED 1|
|J10|Conn_01x03|Duo LED|
|J11|Barrel_Jack_Switch|Barrel_Jack_Switch|
|J12|Conn_01x08|RFID RC522|
|J13|Conn_01x02|Solenoid 12V|
|J14|Conn_01x02|jumper|
|J2|Conn_01x02|Button 2|
|J3|Conn_01x02|LED 2|
|J4|Conn_01x02|Button 1|
|J5|Conn_01x02|Buzzer 12V|
|P8|Conn_02x23_Odd_Even|BeagleBone_Black_Header|
|P9|Conn_02x23_Odd_Even|BeagleBone_Black_Header|
|Q1|Q_NMOS_GDS|STU60N3LH5|
|Q2|Q_NMOS_GDS|STU60N3LH5|
|R1|R|Ω LED1 |
|R14|R|Ω DuoLED|
|R15|R|Ω DuoLED|
|R16|R|100|
|R17|R|2k2|
|R2|R|pull_up|
|R3|R|220|
|R4|R|Ω LED2|
|R5|R|pull_up|
|R6|R|220|
|R7|R|100|
|R8|R|2k2|
|U1|TSR_1-2450|TSR_1-2450|

#### LED resistor notes
Choose the resistors based on the LEDs you use.

|Led |resistors|
| --- | ---: |
|red | 100 ohm|
|green | 60 ohm|
|yellow | 48 ohm|
|blue |4 ohm|


### connected IO ports
| |port|name|
| --- | --- | --- |
|IO|P8_17|Button1|
|IO|P9_12|Solenoid|
|IO|P9_14|UILED1|
|IO|P8_18|Button2|
|IO|P9_17|RC522_SDA|
|IO|P9_22|RC522_SCK|
|IO|P9_18|RC522_MOSI|
|IO|P9_21|RC522_MISO|
|IO|P9_15|RC522_IRQ|
|IO|P9_23|RC522_RST|
|IO|P8_13|UI_DuoLED1r|
|IO|P8_19|UI_DuoLED1g|
|IO|P9_16|UILED2|
|IO|P8_9|Buzzer|


