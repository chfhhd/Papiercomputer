# Papiercomputer - Paper Computer

This is a Word and PDF template of a **Paper Computer**, an educational, non-electronic “computer” made of paper. The template is based on the concept of the original **Know-how-Computer**, also known as **WDR Papiercomputer**, which was presented in 1983 by **Wolfgang Back** and **Ulrich Rohde** in the German TV program *WDR Computerclub*.

With the Paper Computer, simple programs can be written in a minimalist assembly language and executed using matches and a ballpoint pen as “hardware” - completely without electricity or electronics. It is an educational tool that teaches basic concepts of computing and programming in a fun way.

The template does not use the original command abbreviations, but is based on the instruction names definded by [Marian Aldenhövel](https://www.marian-aldenhoevel.de/papiercomputer/), who developed a browser based simulator.

## Architecture and Instruction Set

The template provides 20 memory locations for use as program memory. It also provides 8 registers (A to H) whose contents can be modified with the machine instructions.

The assembly language used comprises the following five instructions.

| Mnemonic | Command | Description |
|----------------|--------------------|--------------|
| `jmp [address]` | Jump to address | Sets the program counter to the specified address. |
| `isz [register]` | Is zero | Checks whether the specified register contains the value 0. If it contains zero, the program pointer is increased by two, otherwise only by one. If there is a zero, the following command is skipped. |
| `inc [register]` | Increment | Increments the value in the specified register by 1. |
| `dec [register]` | Decrement | Decrements the specified register by one and increments the program pointer by 1 if it is greater than 0. |
| `stp` | Stop | Stops the program execution. |

## Usage

1. **Print**: The PDF file is suitable for direct printing. Alternatively, the Word file can be adapted to your needs.
2. **Preparation**: Have matches or small markers ready to represent register states.
3. **Programming**: Enter your program in the space provided. Use the five available commands.
4. **Execute**: Move a ballpoint pen as a program pointer through your program - step by step, command by command.

## Example

One of the basic requirements for the architecture of the paper computer is the ability to set the value of a register to zero. As no separate command is provided for this, this functionality must be implemented manually using a simple program routine.

Accordingly, this example is particularly suitable as an introduction and is often used in courses as a first exercise program:

```
isz A
jmp 3
jmp 5
dec A
jmp 0
stp
```

Possible further exercises are, for example
- copying the contents of register A to register B,
- or adding the values from register A and B.

## Options for expanding the Paper Computer

The Word file can be adapted to your own requirements. For example, a column for labels for jump destinations could be added.

It may also be useful to extend the command set if more complex programs are to be written.

## Further information

There are numerous variants of the paper computer as well as didactically prepared materials and exercise examples on the net. You can find a small selection here:
- [Browserbasierter Simulator von Marian Aldenhövel mit vielen Beispielen (https://www.marian-aldenhoevel.de/papiercomputer/)](https://www.marian-aldenhoevel.de/papiercomputer/)
- [An implementation as a marble computer with extensive didactic material (https://inf-schule.de/rechner/bonsai/murmelrechner)](https://inf-schule.de/rechner/bonsai/murmelrechner)
- [Extensive learning materials on the Paper Pomputer (https://unterrichten.zum.de/wiki/Benutzer:Ukalina/Lernpfad_Know-How-Computer)](https://unterrichten.zum.de/wiki/Benutzer:Ukalina/Lernpfad_Know-How-Computer)
- [The original WDR Papiercomputer (https://web.archive.org/web/20010331082121/http://www.wdrcc.de/khc.phtml)](https://web.archive.org/web/20010331082121/http://www.wdrcc.de/khc.phtml)

## License

This template is licensed under the CC BY-NC 4.0 license. The original idea comes from WDR Computerclub (1983). This implementation is not officially affiliated with WDR or the original developers.
