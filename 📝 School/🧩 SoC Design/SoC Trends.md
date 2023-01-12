Moore's Law
- IC transistor capcity doubles every 18months - 2 years
- 3nm processes (transistor gate lengths) have allowed for the creation of SoCs

- SoCs are basically defined by systems that are interconnected via a protocol.
- Tightly integrated (e.g., Intel modern CPUs) or loosely integrated 

- SoC = Chip + Software + Integration

- SoC Hardware
	- Embedded processor
	- Hardware IPs
	- Peripherals, analog circuitry
	- Embedded memory
	- Interconnect
- SoC Software
	- OS
	- Simulator
	- Firmware
	- Drivers
	- Protocol stacks

 SoCs are like microcontrollers on steroids

# Benefits
- Reduced size
- Reduced system cost
- Lower power consumption
	- Challenging!
- Increased performance
- Increased functionality/performance in reduced footprint
- Simplified PCB design
- Increased product mechanical robustness

# Challenges
- Increasing Complexity
	- Time-to-market pressure
	- Verification bottleneck
 - Integration
	 - HW/SW
	 - Digital vs analog
	 - Testing issues
- Deep submicron problems
	- Timing closure
	- Signal integrity
	- Reliability
- Manufacturing costs

- Being late to the market costs a *lot*

## Bottlenecks
- These days, 50%-80% of development time is done doing verification, even before synthesis/p&r
- Finding the delay of the circuit requires you to P&R first, whereas back in the day you could just sum the gate delays

# Need for new level of abstraction
- RTL well understood, but
	- IP reuse difficult
	- Architectural decision not possible until after RTL verification
	- Level of complexity no longer possible at RTL
	- HDL intrinsically isn't appropriate for algortihm -> circuit, you have to know how the algorithm maps to the circuit first
- Transaction-level modeling (TLM)-IP allows for
	- Design reuse
	- Reduce verification time
	- HW/SW co-verification
	- Function calls instead of cycle accurate
