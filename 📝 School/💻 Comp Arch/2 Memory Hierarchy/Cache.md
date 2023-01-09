## Terminology
- Block (AKA line): Unit of copying
	- May be multiple words
- Hit: Accessed data is present in the upper level (L1)
	- Hit rate: hits/accesses
- Miss: Accessed data not present in upper level
	- Block needs to be copied from lower level (L2 or L3) to upper level
	- Miss rate: misses/accesses = 1 - hit rate
- Miss penalty: Time it takes to copy a block to upper level and deliver it to processor


# Increase Cache Bandwidth
- Pipeline it
- Multibanked caches
	- BW increased by allowing multiple accesses per cycle
	- AKA n-port cache
