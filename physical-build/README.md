<!--
Maintainer:   jeffskinnerbox@yahoo.com / www.jeffskinnerbox.me
Version:      0.0.0
-->


<div align="center">
<img src="https://raw.githubusercontent.com/jeffskinnerbox/blog/main/content/images/banners-bkgrds/work-in-progress.jpg" title="These materials require additional work and are not ready for general use." align="center" width=420px height=219px>
</div>



Wireless print servers are a must-have for home with multiple computers that need to connect to a printer.
I currently have my printer physically paired with my desktop computer and it a pain
to first forward the print job to the desktop for printing.
I'm choosing to create my own print server using a Raspberry Pi.

For printing to happen,
the Raspberry Pi print server must be connected to the same LAN that the print requesting devices are connected to.
In my case this will be my home WAN
and this connection can be via wired Ethernet or wireless WiFi connection.
This will work as long as its into the same network that the Wireless Access Point or Wireless Router serves.

Source
* [How to make a print server with a Raspberry Pi](https://www.xda-developers.com/how-to-make-a-print-server-with-a-raspberry-pi/)

# Raspberry Pi Zero
The physical setup I'm using for my print server is as follows:

* Printer with USB interface - in my case, it was a [HP LaserJet P2035][06]. This printer has the rarely seen USB 2.0 Type-A interface.
* Wireless print server - I used the [Raspberry PI Zero 2 W][07] where I installed the [CUPS print server software][08].
* USB Cable - this allows flexibility for the Raspberry Pi location and [this cable][09] will convert printers female USB 2.0 Type-A to a male USB 2.0 Type-B
* USB Adapter - to convert the male USB 2.0 Type-B to male USB 2.0 Micro-B
* Power the RPi - via USB power plug and male USB 2.0 Micro-B cable

Source:
* [What Are the Different Types of USB Cables?](https://www.anker.com/blogs/cables/how-to-identify-different-types-of-usb-cables-a-brief-guide)

# Raspberry Pi Zero Case
To hold the Raspberry Pi Zero and protect it,
I used the [One Piece Raspberry Pi Zero][02] posted on [Thingiverse][03].
The the files are in the STL format and ready to put thought most any 3D slicer program (e.g. [Cura][05]).

An alternative case is the [Slim Raspberry Pi Zero W Case][04].
In this case, the files are in the 3MF format.

## Convert 3MF to STL
STL (or “stereolithography”) files are the standard 3D file type used for 3D printing.
They describe objects using mosaics or triangular surfaces that fit together to create a single 3D object.
3MF (or “3D manufacturing format”) files also describe 3D objects.
However, unlike STLs, they contain information about cores, materials,
and other details that are not included in the geometry of an STL file.

While the support for 3MF files is growing,
the slow adaptation of this format might require you to convert it to STL at some point.
There is an online site called [SwiftConverter][01] that makes this easy.

Source:
* [3MF to STL: How to Convert 3MF Files to STL](https://all3dp.com/2/3mf-to-stl-how-to-convert-3mf-files-to-stl/)



[01]:https://www.swiftconverter.com/converter.html?threed
[02]:https://www.thingiverse.com/thing:1595429
[03]:https://www.thingiverse.com/
[04]:https://www.printables.com/model/32485-slim-raspberry-pi-zero-w-case
[05]:https://ultimaker.com/software/ultimaker-cura/
[06]:https://support.hp.com/us-en/product/details/hp-laserjet-p2035-printer-series/3662025
[07]:https://www.raspberrypi.com/products/raspberry-pi-zero-2-w/
[08]:https://ubuntu.com/server/docs/install-and-configure-a-cups-print-server
[09]:https://www.commfront.com/products/usb-type-a-to-usb-type-b-cable?variant=13178553091

