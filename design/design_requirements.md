# Design Requirements

1. API requirements
	1. Example program code file
	2. Example data code file
	3. Sample local IO code file
	4. Example remote IO code file 
	5. Example controller code file
2. Target architecture
	1. Windows, 
	2. Linux
	3. embedded Linux, 
	4. bare metal embedded Rust
	5. (Quick reminder that Logix controllers run on VxWorks and the HMIs on WindowsCE, so these targets aren’t as strange as they look)
3. Primary Controller Loop (PCL)
	1. Housekeeping
		1. Remote Communications
		2. Accepting edits
	2. Etc.
	3. Read Inputs
	4. Evaluate and resolve logic
	5. Set outputs
4. Piecemeal compilation of RLC programs, AOIs, UDTs, etc.
	1. In essence, the parts that allow us to perform online edits and enable/disable execution of particular programs and structures