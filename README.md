# QMK Configurator

Fire up https://config.qmk.fm/#/redox/rev1/LAYOUT and load in the json file.

Build firmware in the app, download and extract the source zip.

Build and flash with

    make redox/rev1:ian_qwerty:avrdude

If you have to, manual flashing with a hex image looks like this:

    avrdude -p atmega32u4 -P $(PORT) -c avr109 -U flash:w:$(HEXFILE).hex

e.g.

    avrdude -p atmega32u4 -P /dev/cu.usbmodem14501 -c avr109 -U flash:w:redox_rev1_default_9ea0103.hex
