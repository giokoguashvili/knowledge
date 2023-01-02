# Interrupt Controller Unit

![Interrupt Controller Microarchitecture](https://user-images.githubusercontent.com/8178412/210230269-b5a6ca7f-b2c7-46fd-a043-d546b7ac0a7c.png)


- [PIC - Programmable Interrupt Controller](https://en.wikipedia.org/wiki/Programmable_interrupt_controller) <br/>
 is an integrated circuit that helps a microprocessor (or CPU) handle interrupt requests (IRQ) coming from multiple different sources (like external I/O devices) which may occur simultaneously
- [APIC - Advanced Programmable Interrupt Controller](https://en.wikipedia.org/wiki/Advanced_Programmable_Interrupt_Controller)
  - LAPIC -  Local
  - I/O APIC
- IRR - Interrupt Request Register
- ISR - Interrupt Service Routine
- IMR - Interrupt Mask Register
- IRQ - Interrupt Request
- [ICR - Interrupt Control Register](https://en.wikipedia.org/wiki/Interrupt_control_register)
- ISR - Interrupt Status Register <br/>
    address of each ISR is stored in a fixed location in memory
- [EOI - End Of Interrupt](https://en.wikipedia.org/wiki/End_of_interrupt)

- Hardware Interrupt
  - Maskable Interrupts <br/>
    these interrupts can be delayed when the CPU receives higher priority interrupts
  - Non-Maskable Interrupt
- Software Interrupt

![APIC](https://user-images.githubusercontent.com/8178412/210228890-24b01674-2252-4807-a4a5-9953bf1c90c4.png)

# Sources

- [CSE 306: Operating Systems - Interrupts and System Calls by Don Porter](http://www.cs.unc.edu/~porter/courses/cse306/s16/slides/interrupts.pdf) - pdf
