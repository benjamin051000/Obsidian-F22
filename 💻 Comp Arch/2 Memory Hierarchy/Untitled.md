# Four Questions for Cache Hierarchy
## Block Placement
Where can a block be placed in the upper-level cache?

When cache memory << main memory, multiple memory blocks map to one cache block

- Direct mapped
	- Memory block can be placed in only a single place in cache
	- $cache\ addr = mem\ addr\ \%\ num\ blocks\ in\ cache$
	- Less hardware but more collisions
- Fully associative
	- Memory block can be placed anywhere in cache
	- Less collisions but requires more hardware
	- Associative means that it can figure out which cache location is empty efficiently (parallel hardware)
- Set associative
	- Memory block maps to a set of blocks in cache
	- Place anywhere in set
	- Hybrid of above two


Today no one uses fully associative. Instead they use
- Direct mapped
- 2-way set
- 4-way set
