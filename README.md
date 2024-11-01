![Banner](docs/visual/battiny_banner.png)


![bATtiny Guard Demo Board](docs/visual/battiny_guard_dk_vis1.png)



---------------------------------------------------------------------------------
> [!NOTE]
> "bATtiny Guard" and "PMG001" may be used interchangeably elsewhere in the documentation.

---------------------------------------------------------------------------------
# bATtiny Guard Power management module

bATtiny Guard is a highly integrated module designed for efficient management of single-cell
Li-Po battery systems. It incorporates various essential ICs to address all aspects of power
management, including battery charging, switch/button power on/off behavior, undervoltage
and overvoltage protection, flexible voltage measurement, battery current measurement, and
temperature monitoring. Additionally, it features a microcontroller for programming custom
behaviors, ensuring comprehensive management of single-cell rechargeable battery
systems.
Furthermore, when paired with the demo kit base PCB, the module serves as a general
development board for the ATTINY1616, with all
18 GPIO pins accessible for any application.
&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;


# Features
&nbsp;
&nbsp;
&nbsp;
![Feature overview](docs/visual/info.png)
&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;
<p>
<img src="/docs/visual/battiny_guard_dk_isov.png" align="right" width="35%"/>

- 32 PIN 22.22mm *16.51mm package
- On/off behavior control
- 2A single cell charger
- Single li-po cell powered
- 4+16 ADC channels
- Battery current measurement
- Brown-out detection/reset circuit
- Low on-resistance battery output MOSFET
- On-module temperature measurement
- I2C Interface
- Arduino compatible

<br clear="right"/>
</p>

---------------------------------------------------------------------------------
<p align="left">
  <a href="bATtiny_guard_datasheet.pdf"><img src="docs/visual/badges/Module-Datasheet-1E90FF.svg"></a>
  <a href="docs/schematics/bATtiny_guard_module_schematic.pdf"><img src="docs/visual/badges/Module-Schematic-1E90FF.svg"></a>
  <a href="bATtiny_guard_default_code"><img src="docs/visual/badges/Module-Code-1E90FF.svg"></a>
  <a href="/docs/bom/bATtiny_guard_module_bom_partlist.pdf"><img src="docs/visual/badges/Module-BOM-1E90FF.svg"></a>
</p>

---------------------------------------------------------------------------------
<p align="left">
  <a href="docs/schematics/bATtiny_guard_demo_board_schematic.pdf"><img src="docs/visual/badges/Demo_Board-Schematic-1E90FF.svg"></a>
  <a href="docs/bom/bATtiny_guard_demo_board_bom_partlist.pdf"><img src="docs/visual/badges/Demo_Board-BOM-1E90FF.svg"></a>
</p>

---------------------------------------------------------------------------------

# Installation and set up

To program this module you will need the following:

- Arduino IDE (Or other IDE of your choosing)
- [megaTinyCore](https://github.com/SpenceKonde/megaTinyCore)
- Demo kit with the module soldered on


&nbsp;
&nbsp;
&nbsp;
&nbsp;
<p align="center">
Demo board and cover board views.
</p>
<p align="center">
<img 
    width="45%"
    src="docs/visual/battiny_db_views.png" 
    alt="Demo board views">
</img>
</p>
&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;

There's no need to install any additional libraries as the example code only uses the wire library to handle I2C, the rest is in the [example](bATtiny_guard_default_code/bATtiny_guard_default_code.ino) code. Keep in mind that some register values are hardcoded, which is not the best way to handle something like that but is done here for the sake of simplicity. You can use external libraries with this module without issues, you just need to redefine I2C adresses of devices as they don't necessarily match with other libraries.


&nbsp;
&nbsp;
&nbsp;
&nbsp;

<p align="center">
Board settings should be set up like this:
</p>
<p align="center">
<img 
    width="45%"
    src="docs/visual/arduino_ide_settings.png" 
    alt="settings">
</img>
</p>

Default code provides basic power management and monitoring - press PWR_SW for >500ms and BAT_OUT will turn on, hold PWR_SW for >3s and BAT_OUT will turn off.

To start, you should have the demo board connected via USB to your computer. Powering over USB only will work most of the time, but it is strongly recommended to have the battery connected to the demo board/module.
Switching between USB modes is done with the use of a tactile switch on the demo board; for flashing/programming, set it to 'UPDI', by pressing the button again, the mode is toggled to 'Serial' which will allow for serial communication.
<p align="center">
<img 
    width="45%"
    src="docs/visual/battiny_guard_bat.png" 
    alt="bat connected">
</img>
&nbsp;
&nbsp;
&nbsp;
&nbsp;
<img 
    width="45%"
    src="docs/visual/battiny_guard_usb.png" 
    alt="usb connected">
</img>
</p>
&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;
<p align="center">
Example output to serial (ADC pins floating):
</p>
<p align="center">
<img 
    style="width: 45%;"
    align="center;"
    src="docs/visual/battiny_serial_out_ex.png" 
    alt="settings">
</img>
</p>


For more information, please read the [datasheet](bATtiny_guard_datasheet.pdf).

---------------------------------------------------------------------------------
    
# Module Schematic



![Module schematic](docs/visual/schematic_module_wb.png)

---------------------------------------------------------------------------------


# Demo board Schematic



![Breakout schematic](docs/visual/schematic_breakout_battiny_guard.png)


---------------------------------------------------------------------------------
# bATtiny Series

![bATtiny Series](docs/visual/battiny_series_banner.png)


---------------------------------------------------------------------------------
# [License](LICENSE)

<p align="left">
  
  [<img src="docs/visual/certification-mark-HR000117-wide.svg" style="width: 25%">](https://certification.oshwa.org/hr000117.html)
  
</p>



