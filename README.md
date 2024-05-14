# Rust Logic Controller

1. Free and Open source
2. Lightweight and minimal vertical architecture 
3. Novel logic syntax designed for automation
4. Interact with local IO (GPIO) and network IO (ModBus)
5. Create basic HMIs with {egui, or whatever would work on a little touchscreen (5-7 inches)}
6. Perform online edits and modify logic on-scan
7. Wonderware System Platform-like deployment model of execution and configuration, adapted for a lower level controls schema 
8. Comparable to: the smartest smart relay you ever saw! Seriously, it probably won’t be very complex to start. Blinking lights will be a miracle if the architecture I’m imagining I need to write actually works. 

## Terms

- Logic - specifically the emulated program running on top of the RLC. Analogous to ladder logic or structured text. Hence “logic program” is a program inside the emulated system, etc.
- System, bare metal - the underlying program written in rust that’s executing rust code. The RLC environment runs on top of this. See also System Program
- RLC - the Rust Logic Controller, the emulated system built on top of the system program
- TACL - Thing-Action-Context Language, a programming syntax designed for industrial controls PLC-like programming
- PLC - 
- HMI - 
- IO - 
- ModBus - 
- AOI - 
- UDT - 
- System Program - the underlying programming running the RLC, and doing anything else that rust does. Running the HMI, actual networking and GPIO controls, handling deployments and in deployments, and piecemeal compilation, etc.
- RLC Program - a program written in TACL that is executed in the RLC. Analogous to a controller program in Rockwell’s Logix Designer software.

## Project Goals

1. Primary goal is to be a learning experience
2. Secondary goal is to be usable 
3. Tertiary goal is to be small and portable
4. Quatiery goal is to be competitive

## Summary

Rust Logic Controller is intended to build on the security of Rust by implementing an even more stringent development and runtime environment on top of it: that of the industrial programmable logic controller. On top of Rust an emulated system is built, the Rust Logic Controller. The RLC uses a novel programming language, TACL, to design a PLC-like logic control program in plain text. The syntax of TACL allows for deep automation of code creation and modification. 

## RLC: the Rust Logic Controller

The RLC is intended to be a short stack, I.e. as few jumps as possible between, say, the kernel level code and the “high” level TACL. The programmer should want to use the RLC because it allows them both deep and shallow modification of an overall PLC-like control system. They can write the IO-facing top-level logic in a language that’s suited for it, and optimize or add to the core system programming in a more appropriate and powerful language. 

You’re not locked into a high level PLC language, but you’re also not stuck loading abstractions onto your firmware and software stack just to have a plc-like environment for the code that will change most often: that which modifies the IO.

You can work on embedded programming and controls programming on the same system.

(I should ready more about RTOSs, I don’t much much about them other than the name and that they’re fast. I might be reinventing the RTOS lmao. But we reinvent the wheel not so we have more wheels, but so we have more inventors.)

I encourage this project to emphasize innovative and novel ideas over just implementing existing PLC capabilities. I started this project more for me, and perhaps others, to learn from and have fun with, rather than an actual production application.

As an Independent Constraint on the project I want to impose the challenge of making it as small as possible. As big as necessary, as big as the novelty requires, but focus on making it small too. Focus on size rather than speed, because the requires of the scan time of a PLC are much slower than the underlying system is capable of producing, which is good. So we will raise size slightly above speed. The closer we are to the bare metal, the faster the RLC be, and thus we can be slower and less optimized before impacting the logic executions.

Design requirements:
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