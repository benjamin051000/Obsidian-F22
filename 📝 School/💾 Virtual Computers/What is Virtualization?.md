- Has existed since the 70s, since mainframes existed (large computers used for enterprises)
- Legacy OSes were single-user, single-thread
- Multithreading, multiprocessing, virtual memory, and multi-user emerged over time

# Classical VMs
VMware, VirtualBox, KVM
- Time-share hardware resources

## Hosted VM
- A VM running on a host OS
- Easier to bootstrap VMs
- Expose a VM that is _functionally identical_ to the underlying physical hardware

# Kernel virtualizations
- Conventional OSes expose "virtual" constructs to processes
	- Time-sharing
	- Virtual Address Spaces
	- Block/char devices
	- OS containers


# Modern era
- Virtualization spand beyond a single computer
- Includes networked machines

## Computing Clouds
- AWS EC2 instances
	- Pay-as-you-go dynamic, reconfigurable VMs
	- Pay for virtual CPUs and virtual memory

