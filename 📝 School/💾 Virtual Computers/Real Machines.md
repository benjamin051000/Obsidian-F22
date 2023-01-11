- Resource Management
	- Processor
	- Memory
	- I/O
 
![[Pasted image 20230111095038.png]]
When we look at storage, we are mainly focused on Hard Drives and network.

# Processor
- Finite State Machine
- Typical RISC Pipeline Stages:
	- Fetch, decode, execute, memory write, writeback to register
 - Instruction-level parallelism
	 - Overlap execution of instructions
	 - Superscalar (e.g., Pentium), VLIW (e.g., IA-64)
- Thread-level parallelism
	- Overlap execution of threads
	- Chip multiprocessors, multi-threading
