# Sabina-1 Fifteen Digit Union Square Metronome Clock Replica Nixie Tube Clock
Arduino ATmega 1284P based Nixie clock with GPS, PIR, automatic daylight saving time setting, and many additional features.

From Wikipedia - On the left side of the work is a set of fifteen large LED digits, called "The Passage", which display the time in 24-hour format. The seven leftmost digits show the time in conventional 24-hour format, as hours (2 digits), minutes (2 digits), seconds (2 digits), tenths of a second (1 digit). The seven rightmost digits display the amount of time remaining in a 24-hour day, as tenths of a second (1 digit), seconds (2 digits), minutes (2 digits), hours (2 digits). The center digit represents hundredths of a second, and appears as a blur. For instance, if the clock reads "195641189180304", it means that time is 19:56 (7:56 PM) and 41.1 seconds, and that there are 04 hours, 03 minutes, and 18.9 seconds remaining in the day. 

Sabina-1 is a fifteen digit clock. Several different tubes are supported including Z570M series, IN-14, IN-8-2, and IN-12B. National 8422/5991 tubes will fit the IN-12B board, but should be soldered with pin sockets placed on the tube pins first due to very slight differences in pin spacing. The Z570M Series board also works with the IN-8-2 with careful lead placement, but a dedicated IN-8-2 board has been added as of 10/1/15. Tubes are individually mounted on separate circuit boards, to allow easy replacement and swapping as necessary.

Bugs are corrected as they are found.

Features of the clock include:

• Three configurable heirarchical override periods with independent settings for start and end times, and Nixie brightness. Each period can be enabled for weekdays, weekends, or both. Override button restores standard settings for user selectable time period.

• Real time clock with accuracy to approximately one second per week

• Optional GPS receiver syncs real time clock when variance is one second or greater

• Automatic timezone setting for daylight saving time and standard time

• Scrolling date display with three selectable date formats

• Scrolling temperature display

• Ambient light sensor increases brightness at user configurable setting

• PIR sensor optionally enables display only when motion is sensed, for selected period of time

• Configurable cathode anti-poisoning routing helps to keep tubes in good condition

• Digit change crossfade and vibrate effects

DipTrace schematic, board layouts, acrylic tube spacer .ai files, Arduino code, and operating instructions are included. Latest designs have been ordered from pcbway.com. The processor is an Atmel Atmega 1284P using the Bobuino/Skinny Bob bootloader found here on Github.

GPS - The Ublox Neo-6M and 7M commonly available on eBay for under $15 shipped, works perfectly with this clock. Adafruit Ultimate GPS also works perfectly. The cost is $39.95 plus shipping. Latest versions have a phone jack for the GPS cable, and a header compatible with Ublox boards so that the GPS can be mounted vertically on the clock board. These GPS boards are so sensitive that they work anywhere in the house here in South Florida, so remote placement is not necessary.

Additional Notes:

Individual tube boards are on the Zev-1 page. Only the center digit needs a decimal point to properly display temperature. All tube boards have been updated. The IN-12B has a left-side comma, so the right of center digit comma can be wired to the center digit comma on the board, if you use this tube. 

IN-14, Z570M Series, IN-12B, IN-12BLong, and IN-8-2, are the individual tube boards. Fifteen are required, obviously. The long version IN-12B board rasises tubes by about 10cm. Cut off the tabs for mounting neons and RGB LEDs, if you use this board.

Files with the extension .ai are the designs for the acrylic reflectors. IN-12B tubes use pins easily found on ebay, no acrylic reflectors. Reflectors can be ordered in the USA from Pololu, and at lower cost but obviously longer delivery times from Asian supplies such as Seeed Studio.

Take a look at Zev, my seven and eight digit nixie clock designs, here on Github. Zev-1-7 uses a variety of small tubes same as Sabina, and Zev-2-7, an IN-18 tube version, uses IN-18 tubes. Zev-1-8 and Zev-2-8 are eight digit versions that include nRF24L01+ RF. 

Hex files are used to program the Atmel 1284P chip. Use AVRDude or similar programming tool.

Mitch Feig
