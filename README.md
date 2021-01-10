# Disassembled/commented source code for NES game Bomberman

![JPG](/imgstore/whc4f9a3ebbbf486.jpg)

To compile the .PRG file with DASM, run the following command:

`dasm BMAN.NAS -f3 -oBOMBER.PRG -lBOMBER.LST`

Then you need to concatenate the header, PRG ROM, and CHR ROM into a .NES file. Included are pre-made headers for creating either an iNES ROM (`iNES_Header.bin`) or a NES 2.0 ROM (`NES_Header.bin`)

## For UNIX/Linux/Mac

Run the following command:

### iNES ROM

`cat iNES_Header.bin BOMBER.PRG BOMBER.CHR > BOMBER.NES`

### NES 2.0 ROM

`cat NES_Header.bin BOMBER.PRG BOMBER.CHR > BOMBER.NES`

## For Windows

Run the following command:

### iNES ROM

`copy /B iNES_Header.bin + BOMBER.PRG + BOMBER.CHR /B BOMBER.NES`

### NES 2.0 ROM

`copy /B NES_Header.bin + BOMBER.PRG + BOMBER.CHR /B BOMBER.NES`
