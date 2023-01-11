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


# Interfaces
- ISA: Interface between software and hardware
- ABI: Interface between OS (or) Hardware and user-space software

Advantages
- OS and HW designs are decoupled
- Single app can be designed to run on different OSes
- 

Drawbacks
- Binaries need appropriate system interfaces to work
- Often, apps will not match ABIs and therefore cannot be used

# Virtualization Overview
![[Pasted image 20230111091836.png]]
Software above the coupling layer sees the environment exposed by the coupling layer, not what's beneath it!

# Process vs System VMs
## Process VMs
- Work at ABI interface, seen by applications
- E.g., multi-programmed OSes, containers

## System VMs
- Expose ISA interface
- e.g., classic VMs
### Classic VMs
- Manages hardware resources at all times
- VM Monitor, AKA VMM
- e.g., IBM z/VM, VMware ESX

```ad-question
Is Proxmox considered a classic VM?
```

### Hosted VMs
- VM runs on top of a host OS
- Hardware resource mgmt shared between VMM and host OS
- e.g., VMWare, Virtualbox, etc.

### Other types
- OS-translating VMs
- Whole-system VMs
- High-level language VMs
	- Java JVM
- Co-designed VMs

### OS-translating VMs
![[Pasted image 20230111092637.png]] 
In this image, assuming  you have the same x86 arch, you could run a linux app where linux syscalls are translated into Windows syscalls. Wine is the other way around, windows to linux.

### Whole System VMs
- In "Classic VMs," Multiple OSes run on single machine 
	- As long as all OSes run on ISA of physical machine
- In whole-system VMs, VMs of ISAs different from physical machine are supported.
#### Examples
- E.g., 8/16-bit game console emulators!
	- "Real" previous gen systems
- x86 emulators
	- "real" current gen systems
	- e.g., Bochs, Virtual PC for PowerPC Mac
- Architecture simulators
	- "virtual" current/next gen systems
	- e.g., SimpleScalar, Simics

In general, whole-system VMs are super slow 


### HLL VMs
- ABI VMs
- Exposes its own instruction set, e.g., bytecode
- Tied to a high level language

```ad-question
Is the CPython interpreter also considered a HLL VM?
```

# Taxonomy 
![[Pasted image 20230111093016.png]]
