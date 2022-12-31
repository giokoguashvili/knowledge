# [Computer Organization & Architecture](https://en.wikipedia.org/wiki/Computer_architecture)

- [Arithmometer](https://en.wikipedia.org/wiki/Arithmometer) - by Louis Payen around 1887 <br/>
 was the first digital mechanical calculator strong enough and reliable enough to be used daily in an office environment
- [ENIAC](https://en.wikipedia.org/wiki/ENIAC) - founded in 1945 <br/>
was the first programmable, electronic, general-purpose digital computer

![Screenshot 2022-12-29 161146](https://user-images.githubusercontent.com/8178412/209950291-45616197-40c8-4371-8160-89b8a45255d0.png)

- [Von Neumann architecture](https://en.wikipedia.org/wiki/Von_Neumann_architecture)
- [Harvard architecture](https://en.wikipedia.org/wiki/Harvard_architecture#:~:text=The%20Harvard%20architecture%20is%20a,the%20same%20memory%20and%20pathways.)

# [ISA - Instruction Set Architecture](https://en.wikipedia.org/wiki/Instruction_set_architecture)
![Screenshot 2022-12-29 155012](https://user-images.githubusercontent.com/8178412/209951851-7971d2f6-4ff4-48a6-afa1-c5eb53ab9c0a.png)

Is an abstract model of a computer. A device that executes instructions described by that ISA, such as a central processing unit (CPU), is called an implementation

[Comparison of Instruction Set Architectures](https://en.wikipedia.org/wiki/Comparison_of_instruction_set_architectures) (Platforms)
- [CISC - Complex Instruction Set Computer](https://en.wikipedia.org/wiki/Complex_instruction_set_computer)
    - [x86-64](https://en.wikipedia.org/wiki/X86-64) (Intel/AMD)
- [RISC - Reduced Instruction Set Computer](https://en.wikipedia.org/wiki/Reduced_instruction_set_computer)
    - [ARM - Advanced RISC Machines](https://en.wikipedia.org/wiki/ARM_architecture_family) (Cortex/Snapdragon)
    - [MIPS - Microprocessor without Interlocked Pipelined Stages](https://en.wikipedia.org/wiki/MIPS_architecture) (R4700 - Orion)
    - [SPARC - Scalable Processor Architecture](https://en.wikipedia.org/wiki/SPARC)
    - [PPC - PowerPC - Performance Optimization With Enhanced RISC](https://en.wikipedia.org/wiki/PowerPC)
- [VLIW - Very Long Instruction Word](https://en.wikipedia.org/wiki/Very_long_instruction_word)
    - [e2k](https://en.wikipedia.org/wiki/Elbrus_(computer)) (Elbrus)
- Itanium

List of
- [List of Intel CPU microarchitectures](https://en.wikipedia.org/wiki/List_of_Intel_CPU_microarchitectures)
- [List of AMD processors](https://en.wikipedia.org/wiki/List_of_AMD_processors)
- [List of ARM processors](https://en.wikipedia.org/wiki/List_of_ARM_processors)
- [List of MIPS architecture processors](https://en.wikipedia.org/wiki/List_of_MIPS_architecture_processors)
    

# [Micro-Architecture](https://en.wikipedia.org/wiki/Microarchitecture)
A microarchitecture is a hardware implementation of an ISA (instruction set architecture), is the way a given instruction set architecture (ISA) is implemented in a particular processor

[Comparison of Microarchitectures](https://en.wikipedia.org/wiki/Comparison_of_CPU_microarchitectures)
- Cortex-A57
- Sandy Bridge


## Concepts
- [Instruction cycle](https://en.wikipedia.org/wiki/Instruction_cycle)
- Multicycle microarchitecture
- [Instruction pipelining](https://en.wikipedia.org/wiki/Instruction_pipelining)
- [CPU cache](https://en.wikipedia.org/wiki/CPU_cache)
- [Branch prediction](https://en.wikipedia.org/wiki/Branch_predictor)
- [Superscalar processor](https://en.wikipedia.org/wiki/Superscalar_processor)
- [Out-of-order execution](https://en.wikipedia.org/wiki/Out-of-order_execution)
- [Register renaming](https://en.wikipedia.org/wiki/Register_renaming)
- [Multiprocessing](https://en.wikipedia.org/wiki/Multiprocessing)
- [Multithreading](https://en.wikipedia.org/wiki/Multithreading_(computer_architecture))

# [CPU - Central Processing Unit](https://en.wikipedia.org/wiki/Central_processing_unit)
![Screenshot 2022-12-29 173955](https://user-images.githubusercontent.com/8178412/209962040-d0477f62-f7c6-47ff-9c0c-d811f2b043bc.png)



- CPU
    - [Single cycle processor](https://en.wikipedia.org/wiki/Single_cycle_processor)
    - [Multi-cycle processor](https://en.wikipedia.org/wiki/Multi-cycle_processor)



## [Control Unit](https://en.wikipedia.org/wiki/Control_unit)
- Timing Unit
- Program Counter
- [Instruction Register - IR](https://en.wikipedia.org/wiki/Instruction_register)<br/>
`[MODE | OPCODE | OPRAND]` 
- Instruction Decoder

## [ALU - Arithmetic Logic Unit](https://en.wikipedia.org/wiki/Arithmetic_logic_unit)
![Screenshot 2022-12-30 153401](https://user-images.githubusercontent.com/8178412/210066237-fe038fa3-de2e-43a1-9b59-d74622dfe318.png)

- Multiplexers
- Demultiplexers
- Encoders 
- Decoders

Resources:
- [Combinational logic](https://en.wikipedia.org/wiki/Combinational_logic) - wiki
- [Transistor Gates](http://hyperphysics.phy-astr.gsu.edu/hbase/Electronic/trangate.html) - hyperphysics.phy-astr.gsu.edu
- [Computer Logical Organization Tutorial](https://www.tutorialspoint.com/computer_logical_organization/index.htm) - tutorialspoint.com
- [Digital Electronics Tutorial](https://www.javatpoint.com/digital-electronics) - javatpoint.com


## Memory Unit

- [Processor register](https://en.wikipedia.org/wiki/Processor_register)
- [Cache](https://en.wikipedia.org/wiki/CPU_cache)

## Instruction Cycle
![control-unit](https://user-images.githubusercontent.com/8178412/209962028-b7ea8be5-0321-4a40-88aa-6959fa1f7e58.png)
- fetch
- decode
- execute
- store (write-back)

## [Clock generator](https://en.wikipedia.org/wiki/Clock_generator)
is an electronic oscillator that produces a clock signal for use in synchronizing a circuit's operation
![Screenshot 2022-12-29 180527](https://user-images.githubusercontent.com/8178412/209966681-39087926-f490-4c6c-9857-d9f17f1db1df.png)

# [Computer Memory and Data Storage types](https://en.wikipedia.org/wiki/Computer_memory)
## Memory Types
![Types of Computer Memory (www tutorialsmate com)](https://user-images.githubusercontent.com/8178412/209986220-2f59a8b5-9756-4b90-b43a-9fda749e4aa2.png)
- Volatile
    - [Flip-flop / Latch ](https://en.wikipedia.org/wiki/Flip-flop_(electronics)) (Cache, Register)
    - [SRAM - Static random-access memory](https://en.wikipedia.org/wiki/Static_random-access_memory) (Cache, Registers)
    - [DRAM/RAM - Dynamic random-access memory](https://en.wikipedia.org/wiki/Dynamic_random-access_memory) 
- Non-volatile
    - [NVRAM Non-volatile random-access memory](https://en.wikipedia.org/wiki/Non-volatile_random-access_memory)
    - [ROM - Read-Only Memory](https://en.wikipedia.org/wiki/Read-only_memory)
    - [SSD - Solid-state drive](https://en.wikipedia.org/wiki/Solid-state_drive)
    - [HDD - Hard Drive Disk](https://en.wikipedia.org/wiki/Hard_disk_drive)

## Concepts
- [MMU - Memory Management Unit](https://en.wikipedia.org/wiki/Memory_management_unit)
    - [Virtual memory](https://en.wikipedia.org/wiki/Virtual_memory)
- [Shared Memory Models](https://en.wikipedia.org/wiki/Shared_memory)
    - [UMA - Uniform Memory Access](https://en.wikipedia.org/wiki/Uniform_memory_access#:~:text=Uniform%20memory%20access%20(UMA)%20is,share%20the%20physical%20memory%20uniformly.)
    - [NUMA - Non-Uniform Memory Access](https://en.wikipedia.org/wiki/Non-uniform_memory_access)
    - [COMA - Cache-Only Memory Architecture](https://en.wikipedia.org/wiki/Cache-only_memory_architecture)
    - [HSA - Heterogeneous System Architecture](https://en.wikipedia.org/wiki/Heterogeneous_System_Architecture)
## [Memory Hierarchy](https://en.wikipedia.org/wiki/Memory_hierarchy)
![Screenshot 2022-12-29 210901](https://user-images.githubusercontent.com/8178412/209986366-cd9ab57a-dc72-4e49-9447-453d2d9b3d6e.png)
- Registers
- Cache
- RAM
- SSD/HDD/USB Flash

## [Memory Latency](https://en.wikipedia.org/wiki/Memory_latency#:~:text=Memory%20latency%20is%20the%20time,with%20the%20external%20memory%20cells.)
![MemHierLimits3](https://user-images.githubusercontent.com/8178412/209988610-8b7e4062-d1ba-49bc-911b-e4aa80b7dc21.png)

# [HDL - Hardware Description Language](https://en.wikipedia.org/wiki/Hardware_description_language)
That can model the behavior and structure of digital systems at multiple levels of abstraction, ranging from the system level down to that of logic gates, for design entry, documentation, and verification purposes
- [VHSIC - Very High-Speed Integrated Circuit](https://en.wikipedia.org/wiki/Very_High_Speed_Integrated_Circuit_Program)
- [Verilog](https://en.wikipedia.org/wiki/Verilog) <br/>
- [VHDL - VHSIC Hardware Description Language](https://en.wikipedia.org/wiki/VHDL)<br/>

| Verilog                   | VHDL                  |
| ------------------------- | --------------------- |
| ASIC Deisgns              | FPGA Designs          |
| Weakly Typed              | Strongly Typed        |
| Low Verbosity             | High Verbosity        |
| Partially Deterministic   | Very Deterministic    |
| More "C" like             | Non "C" like          |

# [Transistors](https://en.wikipedia.org/wiki/Transistor) and [Integrated Circuits](https://en.wikipedia.org/wiki/Integrated_circuit)
- [IC - Integrated Circuit](https://en.wikipedia.org/wiki/Integrated_circuit) <br/>
all CPUs are ICs. Not all ICs are CPUs
- [ASIC - Application-specific integrated circuit](https://en.wikipedia.org/wiki/Application-specific_integrated_circuit)
- [FPGA - Field-programmable gate array](https://en.wikipedia.org/wiki/Field-programmable_gate_array)


# Books
- [Digital Design and Computer Architecture - by by David Harris, Sarah Harris](https://g.co/kgs/ptBpJq)
    - [RUS](https://microelectronica.pro/wp-content/uploads/books/digital-design-and-computer-architecture-russian-translation.pdf)
    - [ENG](http://www.csit-sun.pub.ro/courses/cn2/Digital_design_book/Digital%20Design%20and%20Computer%20Architecture.pdf)

# Courses
- [Архитектура ЭВМ Industrial - Software Engineering Online](https://www.youtube.com/playlist?list=PLnseyzyGdZdfv8H7LkvyVVE33fbBZaSdH) - youtube.com
- [Digital Design & Computer Architecture - ETH Zürich (Spring 2020) Onur Mutlu Lectures](https://www.youtube.com/playlist?list=PL5Q2soXY2Zi_FRrloMa2fUYWPGiZUBQo2) - youtube.com
- [Livestream - Digital Design and Computer Architecture - ETH Zürich (Spring 2021) Onur Mutlu Lectures](https://www.youtube.com/playlist?list=PL5Q2soXY2Zi_uej3aY39YB5pfW4SJ7LlN) - youtube.com
![Screenshot 2022-12-29 155058](https://user-images.githubusercontent.com/8178412/209950287-bbf85ded-ce69-4d45-bc1a-fab3bdaa6628.png)
![Screenshot 2022-12-29 161345](https://user-images.githubusercontent.com/8178412/209950294-c62195c4-201a-43cf-acfc-b9428f9bcd33.png)
![Screenshot 2022-12-29 161213](https://user-images.githubusercontent.com/8178412/209950293-2fbf3755-abfe-4292-a68c-c4a0a5056736.png)

