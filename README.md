# BMW Nav Mount To TomTom Adaptor

## Description
These are the design files for an adaptor to allow TomTom sat navs to be mounted on, and powered by, a BMW Nav Mount. The project involves 3D printed components, two PCBs, a 12V/5V converter module and some custom-moulded silicone rubber seals for waterproofing.

## Mechanical Components
The mechanical components are designed using FreeCAD. The model contains the parts for the adaptor and some support components such as the mould and lid for the silicone seals.

### AdaptorBase
Fits to the BMW Nav Mount using the standard locking mechanism. Contains a PCB that connnects to the BMW's 12V supply pins, a magnet to turn on the 12V and two silicone seals to prevent water ingress.

### TomTomMount
Fits into the back of the TomTom. Provides a mechanism for a locator block with locking 'key' so that the TomTom with the mount can be removed from the bike without the rest of the relatively bulky adaptor.

### TomTomLocatorBlock
Fits into the TomTomMount and can be locked to it. Contains a PCB with two pogo pins that supply 5V to the TomTom. A small silicone rubber seal surrounds the pogo pins and should be glued in place.

### InternalSupport
Fits between the TomTomLocatorBlock and the AdaptorBase to keep the TomTom PCB and the BMW PCB in place.

## Electronics
The TomTom and BMW PCBs are designed in KiCad. They are made as a single PCB that needs to be separated before assembly. A 12V/5V buck converter module sits between them.

### BMW PCB
Picks up the 0V and 12V pogo pins from the Nav Mount and provides pads for the wires connecting to the buck converter module. A surface mount LED and current limiting resistor can be fitted to confirm that the 12V is present. This is useful during development but may not be in the final adaptor if the material used for the body is opaque. The PCB holds a silicone seal in place.

It is recommended that the BMW PCB's rear pads are gold plated to improve their lifespan and maintain a low resistance connection. It would also be worth increasing the number of vias on the 0V and 12V tracks.

### TomTom PCB
Requires two pogo pins to be mounted and soldered, plus two wires to the buck converter.

### Buck Converter
Converts the BMW 12V to the 5V required by the TomTom. The module used allows an LED with resistors to be fitted across the output to confirm that the 5V is present.

### Internal Wiring
The wiring between the PCBs and the buck converter needs to be short and follow the openings designed for it, particularly in the InternalSupport component.

## Silicone Seals
The FreeCAD model includes a mould for the three silicone seals. These can be made using two-part silicone resin. A mould lid can be used to control the thickness of the seals, although the innermost part of the BMW PCB seal is open to minimise bubbles.

# Bought-In Parts
TomTom PCB pogo pins: aliexpress. 2mm diameter, 14mm length.
Buck converter: kunkune.co.uk 'Mini Step Down Buck Converter 5-30V, 5V output'
