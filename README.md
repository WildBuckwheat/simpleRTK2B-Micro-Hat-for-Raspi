# simpleRTK2B-Micro-Hat-for-Raspi

Connect an ArduSimple simpleRTK2B Micro (F9P or F9R) to a Raspberry Pi (3 or 4) using this small adapter PCB.

The PCB is intended for [AgOpenGPS](https://github.com/farmerbriantee/AgOpenGPS "github.com/farmerbriantee/AgOpenGPS") users that wish to use a [Micro F9P](https://www.ardusimple.com/product/simplertk2b-micro/ "Ardusimple") with a RaspBerry Pi as an NTRIP base station. There are different ways to use the PCB; one beginner friendly way is to use [RTKBase](https://github.com/Stefal/rtkbase "github.com/Stefal/rtkbase") software in combination with [RTK2go](http://rtk2go.com/ "rtk2go.com").

The PCB can be ordered with the top assembled from JLCPCB SMT service, but you will have to solder the bottom 2x20 header yourself.

<img src="https://github.com/WildBuckwheat/simpleRTK2B-Micro-Hat-for-Raspi/blob/main/Images/Render%203D%20Basic%20BOM.png" width="400"> <img src="https://github.com/WildBuckwheat/simpleRTK2B-Micro-Hat-for-Raspi/blob/main/Images/Render%203D%20Complete%20BOM.png" width="400">



# BOM Files

There are 2 BOMs to choose from. Choose the one that suits your needs.

### BOM Basic
Includes the headers for the Micro, the reset button, the USB plug, and the decoupling caps. That's all you need for RTKBase. There will be lots of empty holes to solder additional headers or wires if you ever want to modify anything. This is the recommended version.

### BOM Complete
Has headers in every hole. You probably won't use most of them and it's just an added expense if ordering using JLCPCB's SMT service. Its there if you want it. If you are hand soldering then you will find the through hole caps on this BOM.



# Features
**Features summary: Powers the Micro, connects the Micro's Serial 1 to the Pi UART, has a USB port if you need it, has a whole bunch of unused pads/headers to allow you to connect other stuff to it.**
1. The Micro is powered from the Pi's 3.3v rail. Decoupling capacitors are included, with pads for both through hole or SMD.
2. The Micro's serial 1 connection is connected to the Pi's UART.
3. A USB mini B port allows for USB connection to a PC running U-Center, etc.
4. A reset buttons allows for reset of the Micro without needing to cycle power to the Pi.
5. SMD 3.3v Power LED
6. The Micro's serial 2 connection is broken out to 4 pin headers. Intended for use with an external radio.
7. All of the Micro's pins are broken out to headers. Intended for easy of modification (you could experiment with the I2C connection).
8. All of the Pi's GPIO are broken out to a header. Intended for ease of modification (you could add an I2C SSD1306 OLED screen).
9. PoE headers for a Pi 4 are included, intended for ease of modification (you could add a voltage regulator between PoE pins and 5v pins).
10. 5v and 3.3v power headers are broken out, intended for ease of modification.
11. The antenna connection is centered in the board where your fingers have the greatest chance of being able to make the SMA connection.
12. The antenna exits the board on the side of the USB connectors. This works nicely with many Raspberry Pi cases. Unfortunately it was not possible to design the board so that the antenna exits above the USB power connection, there just isn't enough room to fit inside a case that way.



# Ordering using JLCPCB's SMT Service

You'll need the Gerber file, the Basic or Complete BOM file, and the Pick and Place (CPL) file. All the JLCPCB default options are ok. 1 oz fill is ok. Snazz it up and change the board colour if you like. Use the SMT assembly service for the Top Side and purchase/solder your own bottom 2x20 header.

Note: It is possible to have JLCPCB solder the bottom header for you, but it is very expensive. In order to process the order you have to select "double sided assembly," and JLCPCB will charge you as if they have to flip the PCB in their pick-and-place machine. To have JLCPCB assemble only the top parts is ~$30 for 5 boards. To have JLCPCB assemble the top and bottom is ~$140 for 5 boards. Make sure to de-select the through-hole caps (C1, C2) if you order double-sided.

If you can't solder at all and really want a board, I recommend posting on the [AgOpenGPS Sales Forum](https://discourse.agopengps.com/c/sales "discourse.agopengps.com/c/sales"). Most people only need 1 board and order 5, someone will hopefully have a spare to sell you.



# Part numbers for 2x20 header

Its just a standard 0.1" 2x20 female header
- LCSC C2977589
- Digikey S9200-ND
- Mouser 710-61304021821
- Cut to length whatever ebay/AliExpress headers you have



# For the Tinkerers
The EasyEDA files are provided. All of the unused pads are called out with headers if you want to order the PCB that way. The design is licensed under CERN-OHL-S-2.0, any improvements or modifications should be made available under the same licence. If you have any suggestions please create a ticket on GitHub.
