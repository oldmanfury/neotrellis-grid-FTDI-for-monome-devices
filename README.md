# neotrellis_teensy_FTDI
neotrellis grid modification with color palette and baud rate selector for use with norns, teletype, ansible, and other monome eco-system devices

This outlines how to modify a neotrellis grid that you have built following instructions from https://github.com/okyeron/neotrellis-monome

You will need to set up an FTDI board as described by https://github.com/mcleinn/neotrellis-monome-for-teletype-via-ftdi  I basically followed his instructions, but found that a huge amount of tweaking / sequencing of events was required to select the appropriate baud rate and get all devices to recognize the grid.  At this point, norns is a little finicky - I find that I have to initialize the grid while connected to my norns shield, then reset the norns to get it to be recognized.  A minor inconvenience that might be fixed in the future.

I made a slot next to the Teensy3.2 for the adafruit FTDI friend, and they fit adequately.  Instructions and pictures below.  Once you set up the FTDI and connect it as shown you might want to flash the Teensy with the code in this repository and try it out prior to taking a dremel tool or file to your enclosure.  I did all my debugging with the FTDI hanging outside the enclosure and didn't burn anything out.

Perhaps one day in the future all monome devices will be able to connect directly to a USB Teensy - some generous capable coders have started this endeavor.  This would obviate the FTDI sub-board.  However, when this day comes the FTDI board and old-school mini-USB connecter are a great way to provide more power to the Teensy than the Teensy allows - replacing the sub-board Steven Noreyko added to the original units.  It should be trivial to switch back to Teensy-only operation and use the FTDI for power only at that point.

Modifying the enclosure and shoehorning in the FTDI isn't too hard.  Start by carefully clipping off the FTDI-friend pin header.

![20210307_104949](https://user-images.githubusercontent.com/2180300/111909092-2127bd00-8a19-11eb-86d9-98523c6f51f2.jpg)

De-solder all pins except the two that we won't use - these are to hold the board in place with a couple of small holes much as those that hold the Teensy in place

![20210307_105010](https://user-images.githubusercontent.com/2180300/111909095-2258ea00-8a19-11eb-92a9-3b828d4f17b9.jpg)

Bend the two pin remnants up as shown 

![20210307_105742](https://user-images.githubusercontent.com/2180300/111909099-24bb4400-8a19-11eb-84fa-01a27418c6b6.jpg)

Notch the case to provide space for the main chip and components - I used a dremel tool that looks like a drill bit - maybe a cutting wheel would work better?  Drill holes that match the two remaining mounting-pins.  I got these wrong the first time, and found that holding the board where it would go and moving side to side and forwards and backwards scratched the pin positions into the surface enough for me to drill them in the right place.

![20210307_114154](https://user-images.githubusercontent.com/2180300/111909103-271d9e00-8a19-11eb-9c63-844fbb061c08.jpg)

Solder short jumper wires as shown - there isn't much room for these, so keep them short like this.  They will provide space between the board and components beneath it - you could put some electrical tape on the bottom of the board too if you're worried about shorting things together, but I haven't had a problem with that (yet).

![20210307_114742](https://user-images.githubusercontent.com/2180300/111909104-284ecb00-8a19-11eb-9842-43a411320ed8.jpg)
![20210307_115118](https://user-images.githubusercontent.com/2180300/111909108-2a188e80-8a19-11eb-907b-049a86a9b7c2.jpg)

Put the case back together.

![20210307_115556](https://user-images.githubusercontent.com/2180300/111909113-2b49bb80-8a19-11eb-8512-58ec77bb3722.jpg)

I will probably drop some screws and spacers on either side of the boards to keep the grid case from bowing this much.
