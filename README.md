# simpleRTK2B-Micro-Hat-for-Raspi

Connect an ArduSimple simpleRTK2B Micro (F9P or F9R) to a Raspberry Pi (3 or 4) using this small adapter PCB.

The PCB is intended for AgOpenGPS users that wish to use a Micro F9P as an NTRIP base station. There are different ways to use the PCB; one beginner friendly way is to use RTKBase software in combination with RTK2GO.

The PCB can be ordered with the top assembled from JLCPCB, but you will have to solder the bottom 2x20 header yourself.


# Features

- The Micro is powered from the Pi's 3.3v rail. Decoupling capacitors are included, with pads for both through hole or SMD.
- The Micro's serial 1 connection is connected to the Pi's UART.
- A USB mini B port allows for USB connection to a PC running U-Center, etc.
- A reset buttons allows for reset of the Micro without needing to cycle power to the Pi.
- The Micro's serial 2 connection is broken out to 4 pin headers. Intended for use with an external radio.

- All of the Micro's pins are broken out to headers. Intended for easy of modification (you could experiment with the I2C connection).
- All of the Pi's GPIO are broken out to a header. Intended for ease of modification (you could add an I2C SSD1306 OLED screen, etc).
- PoE headers for a Pi 4 are included, intended for ease of modification (add a voltage regulator between PoE pins and 5v pins).
- 5v and 3.3v power headers are broken out, intended for ease of modification.

- The antenna connection is centered in the board where your fingers have the greatest chance of being able to make the SMA connection.
- The antenna exits the board on the side of the USB connectors. This works nicely with many Raspberry Pi cases. Unfortunately it was not possible to design the board so that the antenna exits above the USB power connection, there just isn't enough room to fit inside a case that way.

**TLDR: Powers the Micro, connects the Micro's Serial 1 to the Pi UART, has a USB port if you need it, has a whole bunch of unused headers to allow someone to connect other stuff to it.**



# Ordering from JLCPCB

### The Person that is budget oriented and can solder a 2x20 header themselves.
Buy the PCB assembled with only the necessary top parts assembled. You'll have to purchase and solder the bottom 2x20 header yourself. You'll get the headers for the Micro, the reset button, the USB plug, and the decoupling caps. That's all you need for RTKBase. There will be lots of empty holes to solder additional headers or wires if you ever want to modify anything.

Part numbers for 2x20 header (its just a standard 0.1" 2x20 female header)
- LCSC C2977589
- Digikey S9200-ND
- Mouser 710-61304021821
- Or cut your own double row AliExpress/Ebay header to size


- Upload the gerber file to JLCPCB
- Use all the default options (you can change the PCB colour if you want)
- Select the "PCB Assembly" slider
- Use all the default options. Ensure that the Assembly Side is set to "Top Side"
- You can change PCBA Qty to 2 if you wish, if you do you'll receive 2 assembled boards and 3 bare PCB's, it will save you a dollar or two.
- Press Confirm
- Upload the BOM and CPL files
- I don't think the useage description matters, I use Research\Education\DIY\Entertainment -> Programmable Controller HS Code 853890
- Press Confirm
- Ensure all the parts are selected, Press Next
- Verify that the preview looks correct. Press Save to Cart

### The Person that can't solder at all
It is possible to have JLCPCB solder the bottom header for you, but it is very expensive. In order to process the order you have to select "double sided assembly," and JLCPCB will charge you as if they have to flip the PCB in their pick-and-place machine. To have JLCPCB assemble the top parts only is ~$30 for 5 boards. To have JLCPCB assemble the top and bottom is ~$140 for 5 boards. If you can't solder at all and really want a board, I recommend posting on the [AgOpenGPS Sales Forum](https://discourse.agopengps.com/c/sales "discourse.agopengps.com/c/sales"). Most people only need 1 board and order 5, someone will hopefully have a spare to sell you.

### The DIY'er
Buy a bare PCB, order the parts somewhere else and solder them yourself. You'll need the gerber file for your PCB manufacturer and you'll need the BOM to find the parts you need. The BOM has parts from LCSC, but you can cross reference all the parts to digikey or Mouser. The only SMD parts are the decoupling caps (0603 size), but there are pads to use through hole caps instead.

### The Tinkerer
The EasyEDA files are provided. All of the unused pads are called out with headers if you want to order the PCB that way. The design is licensed under CERN-OHL-S-2.0, any improvements or modifications should be made available under the same licence.





[RTKBase](https://github.com/Stefal/rtkbase "github.com/Stefal/rtkbase")
[Micro F9P](https://www.ardusimple.com/product/simplertk2b-micro/m "Ardusimple")
[AgOpenGPS](https://github.com/farmerbriantee/AgOpenGPS "github.com/farmerbriantee/AgOpenGPS")
[AgOpenGPS Sales Forum](https://discourse.agopengps.com/c/sales "discourse.agopengps.com/c/sales")

[I'm an inline-style link with title](https://www.google.com "Google's Homepage")
[I'm an inline-style link with title](https://www.google.com "Google's Homepage")
