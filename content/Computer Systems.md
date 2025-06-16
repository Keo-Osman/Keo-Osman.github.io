#Computer-Science
# Von Neumann Architecture
1. Uses one memory location for both data and instructions.
2. *Requests* next instruction/data from memory with unidirectional address bus.
3. Data or instructions are sent to the CPU via the data bisectional bus. The SPU can send data to be stored in memory via this.
## The CPU
1. ALU
	1. Performs calculations.
2. Control Unit (CU)
	1. Fetches and decodes instructions.
	2. Issue control signals to hardware.
	3. Regulate timing using clock.
3. Clock
	1. Rapidly alternate between 1 and 0 to sync all CPU operations.
4. Registers
	1. Used to store small amounts of data that are needed during processing such as
		1. The address of the next instruction.
		2. The current instruction.
		3. Result of calculations.
	2. Special registers include:
		1. Program Counter.
		2. Memory Address Register.
		3. Current Instruction Register.
		4. Memory Buffer Register.
		5. Status Register.
		6. Accumulator.
5. Bus
	1. Collection of parallel wires to pass data between components.
## Fetch, Decode, Execute Cycle
1. Fetch
	1. The address of the next instructions is fetched from the program counter register.
	2. The program counter is incremented by 1 to point to the next instruction.
	3. The instruction is fetched from memory.
	4. Instruction is put in current instruction register.
2. Decode
	1. The instruction is decoded by the control unit
3. Execute
	1. Instruction is executed.
# Memory and Storage
## SSD
1. Uses flash memory consisting of parallelly wired NOR gates or serially wired NAND gates.
2. Comprised of floating gate transistors.
3. Current is passed along the bit and word line to activate flow of electrons from source to drain.
## Magnetic
1. Contains platters/discs.
2. Coated in a special magnetic coating.
3. Binary data represented by changing magnetic orientation.
4. Read write head for each side of the plater.
## Optical
1. Data ais stored on a single spiral track.
2. Disk rotates at a high speed.
3. Laser head moves across the radius of disc.
4. Made of pits and land.
5. Change form pit to land or vice versa is a 1 as light is reflected differently.

---
---
