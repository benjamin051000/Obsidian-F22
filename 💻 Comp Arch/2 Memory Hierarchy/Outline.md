Memory performance is the current largest bottleneck in computer 

- SRAM is the fastest (1-20ns) but is super expensive
- DRAM a little slower but cheaper (50-100ns) about $3-$6/G
- Flash memory (100-200us) is about $.4/G
- HDDs are cheap but slowwww (5-10ms)


# Memory Hierarchy
- CPU Registers
	- Quick af
- L1-L3 Cache
	- Each one is a little bigger & a little slower
- DRAM Memory
	- Gigabytes but slow
- Disk/Flash
	- TBs but slow


Ideal scenario: 
- Provide the processor with the illusion of large/fast/cheap memory
- Let programs address a memory space that scales to the disk size at high speed

Lab 3 is about caches!
