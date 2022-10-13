# Virtual Memory

- Many programs running concurrently
- All use memory and disk
- Virtual memory gives them the illusion that there is more memory available than there actually is
- Basically, abstracts away which hardware device is holding the memory block
![[Pasted image 20221012101546.png]]
## Addressing
- Need system to help figure out where the memory block is located in physical system
- Virtual addres maps to physical address
	- CPU and OS jointly determine this mapping

Analogous to [[Cache]] concepts:
vm page == cache block
page fault == cache miss

- Bring in pages of memory at a time rather than one address, just like in cache


# Security
Many programs running creates a need for isolation

- Virtual memory helps isolate memory spaces
- Avoids security/reliability problems
- Aids sharing of resources (how?)
