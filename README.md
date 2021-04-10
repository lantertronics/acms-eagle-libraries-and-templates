Here's a set of Eagle files for the benefit of my ECE4450: Analog Circuits for Music Synthesis studnets; hopefully other folks will find them helpful as well.

To use acms_project_starter_template, I recommend copying the schematic file and giving it a new filename and deleting the parts you don't need, but *not* copying the board file. The board file shows where to put mounting holes (3.2 mm = , but otherwise isn't too useful, since once you start adding your own parts, Eagle will just plunk them down one after another in a straight line going downward. If you place your parts on the schematic first and then tell Eagle to make the PCB, the parts will appear in a nice convenient grid pattern on the side of the PCB.

ota_upgraded.lbr and synthdiy_upgraded.lbr are librraries I found elsewhere that didn't want to open in the newest version of Eagle; apparently the name for layer 88 got scrabled as part of the input process. I just changed the layer name to "weird" to get something that would import without error.

The devices in the aaronXXXX.lbr libraries all have the suffix _AARON; I did that so I can find my custom devices quickly.

The capacitors in the eagle library have a little capacitor symbol on the PCB footprint, and have the cap value outside. I prefer to put the cap value inside the symbol footprint, so I made aaroncap.lbr, which has some capacitor footprints with the cap symbol removed and the value placed inside the capacitor.

aaronlibrary.lbr has an oval PCB pad with a little X for the schematic symbol (IOPAD_AARON), a jack symbol on the schematic for off-board jacks where the PCB has a circular pad for the signal and a square pad for the ground (OFFBOARD2JACKALT_AARON), and symbols for the SSM2210 and SSM2220 matched transistor pairs.

I made aaronpot.lbr to handle some potentiometers where I couldn't find a built-in Eagle symbol that exactly matched it. I can't remember exactly what I made it for.
