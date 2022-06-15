# xTool-M1-Playground
Wanting to improve the user experience with the xTool M1 desktop laster cutter and blade cutter. Decided to try rolling my own controller while learning a thing or two. So far, I have no idea what I'm doing.

## OOPS ##
I did a little research and found that USBPcap may not capture all of the USB data. Decided to pick up an inexpensive digital analyzer to try nailing down the communication between the xTool M1 and PC. 

## ./USBPcap/
### pcap files created during/used for testing
* power_on_connect.pcapng
  * Wireshark USBPcap during boot and connectivity of xTool M1
* square_50x50_send.pcapng
  * xTool Creative Space
    * Connected to host
    * Import - square_50x50.png
    * Position of square left at origin (0, 0)
    * Laser settings:
      * Laser flat
      * User-defined material
      * Thickness - 0mm
      * Height raised - No
      * Score
        * Power - 100%
        * Speed (mm/s) - 160
        * Pass - 1
      * Engrave and Cut
        * Left at default values
  * Wireshark
    * start packet capture
  * xTool Creative Space
    * Start
    * Send
    * Wait until xTool M1 beeps after receiving job
  * Wireshark
    * Stop packet capture

## ./svg/
### svg files for testing
* square_50x50.svg
  * 50mm x 50mm square SVG created in Inkscape and saved as a Plain SVG file. 