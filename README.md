# neotrellis_teensy_FTDI
neotrellis grid modification with color palette and baud rate selector for use with norns, teletype, ansible, and other monome eco-system devices

This outlines how to modify a neotrellis grid that you have built following instructions from https://github.com/okyeron/neotrellis-monome

You will need to set up an FTDI board as described by https://github.com/mcleinn/neotrellis-monome-for-teletype-via-ftdi  I basically followed his instructions, but found that a huge amount of tweaking / sequencing of events was required to select the appropriate baud rate and get all devices to recognize the grid.  At this point, norns is a little finicky - I find that I have to initialize the grid while connected to my norns shield, then reset the norns to get it to be recognized.  A minor inconvenience that might be fixed in the future.

I made a slot next to the Teensy3.2 for the adafruit FTDI friend, and they fit adequately.  Instructions and pictures below.  Once you set up the FTDI and connect it as shown you might want to flash the Teensy with the code in this repository and try it out prior to taking a dremel tool or file to your enclosure.  I did all my debugging with the FTDI hanging outside the enclosure and didn't burn anything out.

Perhaps one day in the future all monome devices will be able to connect directly to a USB Teensy - some generous capable coders have started this endeavor.  This would obviate the FTDI sub-board.  However, when this day comes the FTDI board and old-school mini-USB connecter are a great way to provide more power to the Teensy than the Teensy allows - replacing the sub-board Steven Noreyko added to the original units.  It should be trivial to switch back to Teensy-only operation and use the FTDI for power only at that point.
