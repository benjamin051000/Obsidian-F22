Ask stitt:
- Payroll?
	- RA?
		- He hasn't heard anything at all
	- Assume I will be OPS
- I'll record my hours starting today
- Specifics about project
- What is GPS?
- What specifically do you expect of John and I this sem?


# Meeting
- Hardware Abstraction Layer (HAL)
	- AFU abstraction (Intel's terminology)
	- Provides
		- MMIO (need this)
		- DMA (don't care about this for our project)
		- Some other stuff
- Software API that allows C++ code to communicate over the MMIO to an FPGA
- Needs to be ported to the Standalone board
- Going from Zeon + PCIe FPGA -> Just an FPGA SoC
	- We'll be using a soft core processor on it
	- AFU will be a peripheral 
		- Communicate over AXI or Avalon
- Platform designer
	- Intent: Replace functionality of Vivado ?
	- Set up soft processor peripherals/interconnections between them?
	- Generate code for it?
	- Will have to look into this
	- Nij has a template of this!
		- Soft processor + FPGA
			- May not even be using platform designer

- First: Understand how to integrate soft cpu with peripheral
- How to compile software for the soft cpu
- Comfort with Tool Flow for SoC designs on Intel chips 
- May be able to reference reconfig1 MMIO

- On the devcloud, FPGA and CPU share memory
	- No R/W to/from FPGA
	- Just create a software array and give the FPGA the base address.
	- This most likely won't work here
		- If platform designer allows it sure, but it probably won't

See email with template from Nij

**First goal:** Get NIOS created and some software running on it
**Second:** Create a random peripheral that does something
- Fibo calculator, adder, who cares
- Just to understand how the soft processor communicates with the peripheral

# Other goals
- Once we have the NIOS running, install linux on it!
- Does the board have an ethernet port?
	- If so, set it up so we can remotely load designs into the FPGA
		- Basically, divide FPGA into 2 regions
			- Soft processor
			- Peripheral
		- Load bitfile into processor's memory
		- Processor configures other portion of FPGA
	- That would let us do it remotely

- Not sure why Nij isn't interested in using devcloud... but whatever


For now, just work on the Windows machines.

