# Rust Logic Controller

Rust Logic Controller (RLC) is intended to build on the security of Rust by implementing an even more stringent development and runtime environment on top of it: that of the industrial programmable logic controller. The RLC uses a novel, non-IEC-61131 programming language, TACL, to design a PLC-like logic control program in plain text.

## Table of Contents
1. Installation

## Installation
TBD

## Usage
TBD

## Configuration
TBD

## Features
1. Free and Open Source
2. Lightweight and minimal vertical architecture 
3. Novel logic syntax designed for automation
4. Interact with local IO (GPIO) and network IO (ModBus)
5. Create basic HMIs with {egui, or whatever would work on a little touchscreen (5-7 inches)}
6. Perform online edits and modify logic on-scan
7. Wonderware System Platform-like deployment model of execution and configuration, adapted for a lower level controls schema 
8. Comparable to: the smartest smart relay you ever saw! Seriously, it probably won’t be very complex to start. Blinking lights will be a miracle if the architecture I’m imagining I need to write actually works. 

### Project Goals
1. Primary goal is to be a learning experience
2. Secondary goal is to be usable 
3. Tertiary goal is to be small and portable
4. Quatiery goal is to be competitive

## Contributing
TBD

I intend for this project to emphasize innovative and novel ideas over just implementing existing PLC capabilities. I started this project more for me, and perhaps others, to learn from and have fun with, rather than an actual production application.

## Examples
TBD

## FAQs

## Changelog


## Licence
This project is licenced under the Apache 2.0 license.

## Credits
- tokio
- egui

## Contact
TBD if not github

## Appendix A: Glossary
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