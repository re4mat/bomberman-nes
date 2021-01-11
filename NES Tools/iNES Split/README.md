# ines-split
Splits an iNES ROM file (extension `.nes`) to PRG-ROM, CHR-ROM and Trainer data files.

Note: If the PRG-ROM or the CHR-ROM consists of a repeated chunk with a length of a power of two, this program will only extract one instance. For example, the Game Genie iNES file has 4 KiB of PRG-ROM data repeated four times for a total of 16 KiB, so this program only extracts 4 KiB.

Developed with Python 3 under 64-bit Windows.

This program was formerly known as *ines-extract*.

Hint: my [`ines-combine`](http://github.com/qalle2/ines-combine/) does the reverse thing (combines the data files back to an iNES ROM file).

## Command line arguments
Syntax: *output_files* *input_file*

### *output_files*
* `-t` *file* or `--trainer`=*file*
  * copy Trainer data (512 bytes) to *file*
* `-p` *file* or `--prg-rom`=*file*
  * copy PRG-ROM data (16 KiB to 4,080 KiB) to *file*
* `-c` *file* or `--chr-rom`=*file*
  * copy CHR-ROM data (8 KiB to 2,040 KiB) to *file*

At least one output file is required. The files must not already exist (they will not be overwritten).

### *input_file*
  * The iNES ROM file to read.

## Example
Split `smb.nes` to `smb.prg` (PRG-ROM data) `smb.chr` (CHR-ROM data):
```
python ines_split.py -p smb.prg -c smb.chr smb.nes
```

## References
* [NESDev Wiki – iNES](http://wiki.nesdev.com/w/index.php/INES)
* [*Bit Twiddling Hacks* &ndash; Determining if an integer is a power of 2](http://graphics.stanford.edu/~seander/bithacks.html#DetermineIfPowerOf2)
