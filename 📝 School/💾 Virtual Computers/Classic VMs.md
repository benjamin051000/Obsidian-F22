"Classic" means same-ISA system VMs

- VMs support unmodified binaries
- Hosted VMs included

- Not as flexible as whole-system VMs
	- But more flexible than conventional OSes
- Tradeoff between functionality and speed

Can't expect these to run without translation
- Execute non-privileged instructions without translation
	- Performance equivalent to native
- Privileged instructions require translation, emulation
	- To protect virtual machine monitor and other VMs
	- Performance equivalent to emulation
- Overall performance: Amdahl's Law

# Overhead

![[Pasted image 20230111094714.png]]
