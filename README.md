# doorlockd-PCB-BBB

Kicad drawing for doorlockd electronics on a Beagleboard black cape.

### component list
<pre>
C1	1uF Keramisch
C2	1uF Keramisch
C3	470u
D1	LED
D2	1N4007
J1	Conn 01x02
J10	Conn 01x03
J11	Barrel Jack Switch
J12	Conn 01x08
J13	Conn 01x02
J14	Conn 01x02
J2	Conn 01x02
J3	Conn 01x02
J4	Conn 01x02
J8	Conn 01x02
P8	BeagleBone Black Header
P9	BeagleBone Black Header
Q1	STU60N3LH5
R1	R         (ui led 1)
R11	R         (ui bicolor led) 
R14	R         (ui tricolor led red)
R15	R         (ui tricolor led green)
R16	R         (onboard led) 
R17	R         
R2	pull up   (button 1)
R3	220 ohm   (button 1)
R4	R         (ui led 2)
R5	pull up   (button 2)
R6	220 ohm   (button 2)
U1	TSR 1-2450
</pre>

### connected IO ports
<pre>
IO P8_23 Button1
IO P9_14 Solenoid
IO P8_34 UILED1
IO P8_21 Button2
IO P9_17 RC522_SDA
IO P9_22 RC522_SCK
IO P9_18 RC522_MOSI
IO P9_21 RC522_MISO
IO P9_15 RC522_IRQ
IO P9_23 RC522_RST
IO P8_46 UI_BiLED1r
IO P8_45 UI_BiLED1g
IO P9_28 UI_TriLED1r
IO P9_42 UI_TriLED1g
IO P8_36 UILED2
</pre>
