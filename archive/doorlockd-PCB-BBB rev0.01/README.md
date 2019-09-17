# Info on PCB deuropener rev0.01

## Preview 
<img src="https://raw.githubusercontent.com/wie-niet/doorlockd-PCB-BBB/master/archive/doorlockd-PCB-BBB%20rev0.01/preview-pcb-rev0.01.png" alt="Preview doorlockd-PCB-BBB Rev0.01">

<object data="https://github.com/wie-niet/doorlockd-PCB-BBB/raw/master/archive/doorlockd-PCB-BBB%20rev0.01/preview-schematic-rev0.01.pdf" type="application/pdf" >
    <embed src="https://github.com/wie-niet/doorlockd-PCB-BBB/raw/master/archive/doorlockd-PCB-BBB%20rev0.01/preview-schematic-rev0.01.pdf">
        <p>PDF Preview of Schemantic <a href="https://github.com/wie-niet/doorlockd-PCB-BBB/blob/master/archive/doorlockd-PCB-BBB%20rev0.01/preview-schematic-rev0.01.pdf">preview-schematic-rev0.01.pdf</a> on github.</p>
    </embed>
</object>



## Notes/Bugs: 

### Wrong pins used. [Issue #2](https://github.com/wie-niet/doorlockd-PCB-BBB/issues/2)

Disable the onboard harware in `/boot/uEnv.txt`:
```
	disable_uboot_overlay_video=1 
	disable_uboot_overlay_emmc=1
	disable_uboot_overlay_audio=1
```
### 12V barreljack connected to wrong pin. [Issue #1](https://github.com/wie-niet/doorlockd-PCB-BBB/issues/1)
Quick fix is to create a bridge between pin3 and pin2 of the 12V barreljack.


## GPIO
```
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
```

## Components 
```
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
```


