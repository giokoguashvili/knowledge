# [Assembly](https://en.wikipedia.org/wiki/Assembly_language)


- [NASM - Netwide Assembler](https://en.wikipedia.org/wiki/Netwide_Assembler) (Intel)
- [GAS - GNU Assembler](https://en.wikipedia.org/wiki/GNU_Assembler) (AT&T)
- MASM - Microsoft Assembler
- TASM - Borland Turbo Assembler



# [x86 Assembly/GNU assembly syntax](https://en.wikibooks.org/wiki/X86_Assembly/GNU_assembly_syntax)

Install [GNU Binutils](https://www.gnu.org/software/binutils/)
- **ld** - GNU linker
- **as** - GNU assembler
- **gold** - a new, faster, ELF only linker
- **gdb** - GNU Debugger

> `sudo apt install binutils`

Prefixes
- % - when referencing a register 
- $ - constant numbers need to be prefixed
```
$name
$27
```
Operation Suffixes
- b = byte (8 bit).
- s = single (32-bit floating point).
- w = word (16 bit).
- l = long (32 bit integer or 64-bit floating point).
- q = quad (64 bit).
- t = ten bytes (80-bit floating point).

Registers

```
%eax
%ebx
%ecx
%edx
%esi
%edi
```

Commands
```
mov
cal
int
jmp
```

# Sources
- [Assembly Programming Tutorial](https://www.tutorialspoint.com/assembly_programming/assembly_tutorial.pdf) - tutorialspoint.com

