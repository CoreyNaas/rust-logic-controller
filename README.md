## Project Proposal for Rust Logic Controller

Greetings Rust enthusiasts and Industrial control enthusiasts! We are inviting potential contributors to our open source project Rust Logic Controller. Our project invites those who are passionate about amalgamating the space of Rust and conventional industrial control systems to construct a unique soft Programmable Logic Controller (PLC) with its primary deployment platforms being consumer Windows and Linux machines (ModBus) along with budget-friendly embedded controllers (GPIO and ModBus).

### About the Project

Rust Logic Controller is an open-source initiative that integrates the features like:

- Lightweight and streamlined vertical architecture.
- A bespoke logic syntax algorithm tailored for automation.
- Capability to interface with local IO (GPIO) as well as Network IO (ModBus).
- Creation of rudimentary Human Machine Interfaces (HMIs) adaptively suitable for small touchscreen displays (5-7 inches).
- Ability to conduct online edits and applies logic modifications on-scan.
- Deployment model for execution and configuration is reminiscent of WW, but specifically modified for the lower-level control schemes.
 
The design of this infrastructure can be best compared to the most intelligent smart relay. At its nascent stage, it may not be deeply intricate. Lighting up the "Blinkenlights" will seem miraculous if the conceptualized architectural framework indeed operates as expected.

### Terminology and Definitions

Check out some commonly used terms in the context of our project:

- Logic: The simulated program executing over the Rust Logic Controller (RLC), akin to ladder logic or structured text, hence “logic program” implies a program within the simulated system, and so forth.
- Bare Metal System: This refers to the base program composed in Rust that is executing Rust-written codes. The RLC environment operates over this system.
- RLC: The Rust Logic Controller, the simulated system constructed on top of the system program.
- TACL: Thing Action-Context-Language, this is a programming syntax engineered for industrial controls PLC-like programming. 

### Project Aims

Our project goals which we aim to achieve are as follows:

- Primary Aim: To serve as a learning experience.
- Secondary Aim: To build something usable.
- Tertiary Aim: To develop a small and portable tool.
- Fourth Aim: To be competitive in the space.

### Project Synopsis 

The Rust Logic Controller is envisaged to augment the security features of Rust by establishing a more rigorous runtime environment and development environment on top of it, similar to an industrial programmable logic controller. The Rust Logic Controller (RLC) is built upon Rust, and it employs a novel programming language, TACL, to construct a PLC-like control program in a simple text format. The syntax of TACL facilitates deep automation of code generation and modifications.

### Get Involved 

If the aspects of embedded programming and controls programming on a unified platform intrigue you, please feel free to contribute to our project! Rather than plainly re-implementing existing PLC functions, we encourage innovative and out-of-the-box concepts. We conceived this project mainly as a means of gaining knowledge and having fun rather than a company-oriented application.

We are focusing on making this project as compact as possible. We want to make it as big as necessary for the novelty and as compact as we can. We prioritize size over speed since the scan time requirements of a PLC are significantly slower than what the underlying system can deliver. Our primary design requirements are attached below, including various examples and target architectures. 

### How to Contribute 

1. Fork the repository
2. Make the changes/additions to your forked repository
3. Submit a pull request with detailed comments about the changes

We look forward to your contributions and can't wait to see this open-source project grow and succeed with your help!