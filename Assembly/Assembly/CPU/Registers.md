
These are internal memory locations, used as "variables."

The values of registers keep on changing depending upon what the CPU is doing.



# CPU Registers

Any register in a 32-bit architecture is 32 bits long. Similarly, any register in a 64 bit is 64 bits long.
We use an x86_64 bit architecture, so most of our intel chip code will be in that form.
However, for this "course" most code examined is 32 bit.

> Tip : 32 bit registers are named as *eax, ebx, ecx* etc.
> Whereas their 64 bit counterparts are named *rax, rbx, rip* etc.


## General Purpose Registers

The general purpose registers are further subdivided into 3 categories: 
A. Data Registers
B. Index Registers
C. Pointer Registers

#### Data Registers 
1. EAX : 
	Accumulator Register
		 used for storing operands and result data.

 2. EBX : 
	 Base Register
		 used for storing pointers to the data.

3. ECX : 
	Counter Register
		used in loop operations and string operations.

4. EDX : 
	Data Register
		used in input/output operations.
		Often used along with the AX register to multiply/divide large quantities. (this is for the DX register)


###### Selective Access in Data registers
The first 16 bits of this can be accessed using referencing it as AX.
The first and last bits of AX can be accessed by referencing them as AL (0-7) and AH(8-15)
Similarly for EBX/ECX/EDX as BX, BL , BH and so on.

#### Index Registers
1. ESI and EDI
	Source Index and Destination Index Registers
		Data pointer registers used for memory operations. (usually for string operations)
		SI and DI are the rightmost 16 bit portions of them, and are used for indexed addressing and sometimes in addition and subtraction.

#### Pointer Registers:
1.  ESP 
	Stack pointer Register
		always points to the top of the stack (that is, the lowest memory location available to the stack.)

2. EBP
	Base Pointer Register
		Helps in referencing the parameters passed to a subroutine. (I'm not sure what that means just yet, more on this later) #revise

3. EIP 
	Points to the instruction the CPU is running in the moment.
	**From an exploitation viewpoint, this is one of the most important registers. We shall try to control this.**


## Segment Registers

More on these later #edit

1. CS
	code segment
2. DS
	data segment
3. SS
	stack segment
4. ES, FS, GS
	Generally pointers used for other segments are here.

## Control Registers

More on these later too #edit 

Are internal to the CPU and are used for various calculations.

