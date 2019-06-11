# doorlockd-PCB-BBB

Kicad drawing for doorlockd electronics on a Beagleboard black cape.

### component list
<pre>
C1    1uF Keramisch
C2	   1uF Keramisch
C3	   470u
D1	   LED
D2    1N4007
J1    Conn 01x02
J10	Conn 01x03
J11	Barrel Jack (Switch)
J12	Conn 01x08
J13	Conn 01x02
J14	Conn 01x02 + Jumper 
J2	   Conn 01x02
J3	   Conn 01x02
J4	   Conn 01x02
J8	   Conn 01x02
P8	   BeagleBone Black Header (Conn 23x02 backside of print) 
P9	   BeagleBone Black Header (Conn 23x02 backside of print) 
Q1	   STU60N3LH5
R1	   100 ohm   (ui led 1)
R11	R         (ui bicolor led) 
R14	R         (ui tricolor led red)
R15	R         (ui tricolor led green)
R16	100 ohm   (onboard led) 
R17	2k2 ohm         
R2	   pull up   (button 1)
R3	   220 ohm   (button 1)
R4	   100 ohm   (ui led 2)
R5	   pull up   (button 2)
R6	   220 ohm   (button 2)
U1	   TSR 1-2450
</pre>

UI Led resistors:
red LED 100 ohm
green LED 60 ohm
yellow LED 48 ohm
blue 4 ohm

### connected IO ports
<pre>
   P8_01/02 GND
IO P8_21 Button2     ( MMC1_CLCK )
IO P8_23 Button1     ( MMC1_DAT4 )
IO P8_34 UILED1      ( LCD_DATA11 )
IO P8_36 UILED2      ( LCD_DATA10 )
IO P8_45 UI_BiLED1g  ( LCD_DATA0 )
IO P8_46 UI_BiLED1r  ( LCD_DATA1 )


   P9_01/02 GND
   P9_03/04 +3V3
   P9_05/06 +5V
IO P9_14 Solenoid
IO P9_15 RC522_IRQ
IO P9_17 RC522_SDA
IO P9_18 RC522_MOSI
IO P9_21 RC522_MISO
IO P9_22 RC522_SCK
IO P9_23 RC522_RST
IO P9_28 UI_TriLED1r ( MCASP0 .. (audio?) )
IO P9_42 UI_TriLED1g ( mcasp0_pins (audio?) )
   P9_43..46 GND
</pre>


## Oops.. Rev. V0.01 bugs:
### Wrong GPIO PINs
I've used some already used pins by the onboard hardware.
to enable these pins you need to disable the onboard harware in <code>/boot/uEnv.txt</code>

To enable UILED1 and 2, and the  bicolor LED disable HDMI support:
<pre> disable_uboot_overlay_video=1 </pre>

To enable button1 and 2 , disable internal Flash disk, you need to boot from SDcard:
<pre> disable_uboot_overlay_emmc=1 </pre>

To enable Tricolor LED , disable internal audio:
<pre>disable_uboot_overlay_audio=1 </pre>

### barrel jack footprint 
pin1 12V
pin2 GND
pin3 ...

(quick fix , create bridge between pin3 and pin2)

