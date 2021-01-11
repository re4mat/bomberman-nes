# Disassembled/commented source code for Bomberman (NES)

![JPG](/Images/README.png)

To compile the .PRG file with DASM, run the following command:

`dasm Bomberman.asm -f3 -oBomberman.prg -lBomberman.lst`

Then you need to concatenate the header, PRG ROM, and CHR ROM into a .NES file. Included are pre-made headers for creating either an iNES ROM (`iNES_Header.bin`) or a NES 2.0 ROM (`NES_Header.bin`)

## For UNIX/Linux/Mac

Run the following command:

#### iNES ROM

`cat iNES_Header.bin Bomberman.prg Bomberman.chr > Bomberman\ \(USA\).nes`

#### NES 2.0 ROM

`cat NES_Header.bin Bomberman.prg Bomberman.chr > Bomberman\ \(USA\).nes`

## For Windows

Run the following command:

#### iNES ROM

`copy /B iNES_Header.bin + Bomberman.prg + Bomberman.chr /B "Bomberman (USA).nes"`

#### NES 2.0 ROM

`copy /B NES_Header.bin + Bomberman.prg + Bomberman.chr /B "Bomberman (USA).nes"`

## Checksum of compiled ROM (crc32)

iNES: `b9804046`

NES 2.0: `f5daaf10`
