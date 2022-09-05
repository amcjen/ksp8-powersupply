# ksp8-powersupply
A replacement power supply PCB for the Kurzweil KSP8

Really simple drop-in replacement for the ancient power supply that comes with the KSP8. Included are the v9.0 compatible Eagle
.sch and .brd files, as well as the raw gerbers. The zip file has all the gerbers compressed, and you can usually upload the zip
file directly to most board houses for manufacture.

If you start hearing whining from the power supply transformer, or your unit begins resetting randomly, then it's probably the
power supply, and it's probably time to replace it.

Luckily the great people at Traco make super simple drop-in power supply modules. This board simply adds the right layout, the
proper fuses, and mimic's the power-good circuit that the KSP8 expects to see (though in reality it's likely not even necessary).

The new power supply input specs are super wide, so should be usable pretty much anywhere in the world:

Voltage input:
90-240V VAC
47-440 Hz

Do of course be extremely careful with the mains power coming into this! There are several exposed leads and test points.

Regardless, most of the instructions are on the back of the board, on the silkscreen. It's reproduced here for reference:


JP1 - Tie mains gnd to 5V DC gnd (default: connected)
JP2 - Tie /pwr_ok to voltage supervisor output (default: connected)
JP3 - Tie /pwr_ok to 5V DC gnd (default: disconnected)

TO RUN WITH POWER SUPERVISOR (default):
- Place U3 and R1
- Leave JP2 uncut
- Leave JP3 open

TO RUN WITHOUT POWER SUPERVISOR:
- Exclude U3 and R1
- Cut JP2
- Solder JP3

U1 - Traco TML-40105 - 5V/8A output
U2 - Traco TML-40215 - +15V/1.3A / -15V/1.3A
U3 - Microchip MIC810LUY power supervisor
F1/F2 - Littelfuse 05200101Z - 1.6A slow blow 5x20mm 250V fuses
R1 - 100k 1206 resistor



You can buy Tracos at several retailers, like Mouser and Digikey. Yes, they're pricey, but they are also medical grade, have
excellent electrical specs and clean power, and have something like a 70 year mean time between failure (MTBF). So these should
definitely outlast the device (or at least the LCD!)

One last wonderful side benefit is that these supplies seem to run pretty cool, so no need to have that loud fan running anymore.
Feel free to unplug it from the front board for a more silent studio environment.

✨ Happy music making! ✨


