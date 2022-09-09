# Data-level parallelism

Flynn's Classical Taxonomy

- SIMD: Single Instruction, Multiple Data
	- e.g., Vector processors, GPUs
- MIMD: Multiple Instruction stream, Multiple data stream
	- Most general parallel arch
	- e.g., Comuting clusters, HPC systems

## Principle of Locality
- Programs tend to spend 90% of time in 10% of code
	- Possible to predict what program will do next
- Program tends to reuse data it has used recently
	- Can predict what data a program will use soon
		- Use of data caches

### Two types of locality
- Temporal locality
	- Recently accessed items are likely to be accessed again
- Spatial locality
	- Items whose addresses are near another tend to be referenced at the same time
		- e.g., array items
