#  [I/O Hardware](https://en.wikipedia.org/wiki/Input/output)

## I/O devices can be divided into two categories
- Block devices <br/> 
is one with which the driver communicates by sending entire blocks of data. For example, Hard disks, USB cameras, Disk-On-Key etc
- Character devices <br/>
is one with which the driver communicates by sending and receiving single characters (bytes, octets). For example, serial ports, parallel ports, sounds cards etc

## Device Controllers <br/>
Device **drivers** are software modules that can be plugged into an OS to handle a particular device. Operating System takes help from device drivers to handle all I/O devices

## Synchronous vs asynchronous I/O
- Synchronous I/O <br/> 
In this scheme CPU execution waits while I/O proceeds

- Asynchronous I/O <br/> 
I/O proceeds concurrently with CPU execution

## Communication to I/O Devices

- Special Instruction I/O <br/>
uses CPU instructions that are specifically made for controlling I/O devices. These instructions typically allow data to be sent to an I/O device or read from an I/O device

- [MMIO - Memory-mapped I/O](https://en.wikipedia.org/wiki/Memory-mapped_I/O) <br/>
the same address space is shared by memory and I/O devices. The device is connected directly to certain main memory locations so that I/O device can transfer block of data to/from memory without going through CPU

- PMIO - Port-Mapped I/O

- [DMA - Direct Memory Access](https://en.wikipedia.org/wiki/Direct_memory_access) <br/>
Slow devices like keyboards will generate an interrupt to the main CPU after each byte is transferred. If a fast device such as a disk generated an interrupt for each byte, the operating system would spend most of its time handling these interrupts. So a typical computer uses direct memory access (DMA) hardware to reduce this overhead

- Polling I/O <br/>
is the simplest way for an I/O device to communicate with the processor. The process of periodically checking status of the device to see if it is time for the next I/O operation, is called polling

- Interrupts I/O <br/>
An alternative scheme for dealing with I/O is the interrupt-driven method. An interrupt is a signal to the microprocessor from a device that requires attention

## [UART - Universal Asynchronous Receiver-Transmitter](https://en.wikipedia.org/wiki/Universal_asynchronous_receiver-transmitter)