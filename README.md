# Thinkpad OLKB Preonic keybaord pcb

Get it printed and enjoy.

USB can be connected in multiple ways:

- Directly into the MCU thanks to open space near it
- After soldering the bottom pads, via available pins next to the usb port
- After soldering the bottom pads and FPC connector, via FPC connector

USB can be fetched from multiple places, the lower end the laptop (x series) the less options so I'll list all the w530 options:

- Bluetooth connector, if you swapped wifi card for wifi+bt you aren't using the standalone bt so you can get usb from there
- msata, its next to the open hole for the usb, with msata to usb converter you can either just plug in short cable from msata directly to mcu (easiest possible connection) or you can cut the microusb end and solder it to pins or desolder the usb and route it with wires
- Smartcard fpc connector, it's located at the bottom middle of the motheboard next to the bios chips underneath the touchpad. Thats what the FPC connector on keyboard is for, you can buy 6 pin 0.5mm pitch FPC cable and connect it. Watch out though because it has 5V 15A unfused and if you short it you will instantly kill the laptop, but the keyboard has fuse which protects it, but only if something happens AFTER the fuse so isolate the fpc connector pins.
- Fingerprint/color sensor usb FPC, they're both just usb's on FPC tape, so you can use that, although they might not be directly pluggable into keyboard's FPC connector, I don't know their pinout as I was targetting the Smartcard FPC connector.

Power button is connected via mounting OG keyboard's FPC tape or soldering it, you can pick either option by soldering the pads next to the FPC pins. Make sure you pick correct option otherwise you can short something. Power button is also routed to the mcu pin in case you want that, although when laptop is off, they keyboard is off unless you route always-on 5V to it.

There are pins for connecting Framework touchpad, if you go this route, just wire them to the test pads on the Framework's touchpad and that's it. If you want to use Framework's touchpad and mount it by demeling the case then you need to break out the touchpad pcb extension.

There's hole for a keyboard mounting screw, M2x20 and use a nut to hold it down but don't overtighten it!

Oh also cake the bottom in electrical tape and make sure there are no pointy solder points, otherwise it will short out on the aluminum case which is less than ideal.

As of now the space above keyboard is not covered by anything which is KIIIIIIINDA sketchy but can be covered with electrical tape or simple 3D print. If you don't use the hole for usb cable that one can also be covered via electrical tape.

# BOM 

- FPC 6PIN 0.5mm pitch, same side
- 6 pin FPC connector
- Raspberry pi pico
- PG1425 switches
- Patience

# Gallery

## Schematic

![Schematic](docs/schematic.png?raw=true) 

## Board

![Board](docs/board.png?raw=true) 

## 3D View

![3D View](docs/3d_a.png?raw=true) 

![3D View](docs/3d_b.png?raw=true) 

## Real photo

![Real photo](docs/real.png?raw=true) 
