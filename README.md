## Adafruit WCH CH9102F Friend - USB to Serial Converter PCB

<a href="http://www.adafruit.com/products/5568"><img src="assets/5568.jpg?raw=true" width="500px"><br/>
Click here to purchase one from the Adafruit shop</a>

PCB files for the Adafruit WCH CH9102F Friend - USB to Serial Converter. 

Format is EagleCAD schematic and board layout
* https://www.adafruit.com/product/5568

### Description

Long gone are the days of parallel ports and serial ports. Now the USB port reigns supreme! But USB is hard, and you just want to transfer your everyday serial data from a microcontroller to computer. What now? Enter the Adafruit CH9102F Friend, a version of our popular USB-Serial 'friend' breakouts that uses the affordable (and available) CH9102F - a 'near pin-compatible' to the CP2102N.

This board features the CH9102F USB-Serial chip that can upload code at  3Mbit/s for fast development time. It also has auto-reset for Arduino/ATmega328 boards so no noodling with pins and reset button pressings. The CH9102F has fairly good driver support, and for 99% of use cases is a fine replacement of the FTR232, FT231x or CP210x series. With a modern USB Type C connector, it's ready to rock on any kind of computer.

Some things we've noted as we have been working with this board:

The RX LED blinks as you expect when data is received, however the TX LED does not blink constantly. Instead after a few seconds of data transmission the LED will blink slowly.
On Linux, the CTS pin is not supported by the built in Linux kernel driver. Oddly enough, all the other flow control pins work perfectly fine - its just CTS that doesn't. You can fix it by installing an out-of-tree driver which we did on a Raspberry Pi. Fortunately, for uploading code to microcontrollers, almost all of them use RTS/DTR for auto-resetting so not having CTS isn't a big deal.
By default, we've set it up so that it matches our FTDI cables. The 6th pin is RTS, the power wire is +5V, and the signal levels are 3.3V (they are 5V compliant and should work in the vast majority of 3.3V and 5V signal systems). Works excellently with any Arduino, ESP8266, ESP32, or any other microcontroller that uses an 'FTDI port' for communications and upload. You can also purchase a 6-pin extension cable from us, which will let you rearrange the wire order.

There's also a full collection of all the modem control pins you may need on the side, in case you need the DTR, RI, DSR, etc. pins.

Each order comes with a fully assembled and tested board. We give you a right-angle socket header and some male header strip. You can solder in the socket header on the edge to make it 'FTDI-like' or solder the male headers in to plug it into a breadboard and get access to all the pins.

For Linux, you won't need a driver (unless you happen to need CTS support, see above).

For Windows and MacOS X, check our tutorial page on how to install drivers.

### License

Adafruit invests time and resources providing this open source design, please support Adafruit and open-source hardware by purchasing products from [Adafruit](https://www.adafruit.com)!

Designed by Limor Fried/Ladyada for Adafruit Industries.

Creative Commons Attribution/Share-Alike, all text above must be included in any redistribution. 
See license.txt for additional details.
