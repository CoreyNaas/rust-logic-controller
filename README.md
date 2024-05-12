# Proposal for Rust Logic Controller Project Engagement

## Introduction to Rust Logic Controller

The Rust Logic Controller (RLC) project seeks innovative collaborators interested in the intersection of Rust programming and industrial control system practices. The mission is to create a soft Programmable Logic Controller (PLC) that's not only free and open-source but also lightweight with a minimal vertical architecture. This unique initiative aims to combine the robust security features of Rust with traditional automation systems, targeting Windows and Linux consumer machines through ModBus protocol and budget embedded controllers via GPIO and ModBus.

## Innovative Features of RLC

RLC offers a distinct syntax tailored for automation, allowing interaction with both local (GPIO) and network I/O (ModBus). It enables the development of basic Human-Machine Interfaces (HMIs) suitable for small touchscreens while providing the flexibility to perform online edits and logic modifications during operation. The deployment model is inspired by Wonderware-like execution but tailored to lower-level control schemas. In essence, RLC could be likened to an exceptionally intelligent smart relay, albeit with modest initial complexity, aiming for a 'blinkenlights' level of functionality as a testament to its architecture's success.

## Glossary

- RLC: Rust Logic Controller, an emulation layer atop the system program.
- TACL: Thing Action-Context-Language, a novel syntax for PLC-like programming.
- PLC: Programmable Logic Controller.
- HMI: Human-Machine Interface.
- IO: Input/Output interface for systems.
- ModBus: A communication protocol commonly used in industrial settings.
- AOI: Add-On Instruction, reusable code blocks in PLCs.
- UDT: User-Defined Type, data structures for PLCs.
- System Program: The Rust-based foundation managing the RLC, including HMI, networking, GPIO control, deployment, and real-time compilation.

## Project Goals

1. To serve as a comprehensive learning experience for contributors.
2. To develop a functional and usable soft PLC system.
3. To ensure the project remains small, portable, and easy to deploy.
4. To achieve competitiveness within the scope of its design parameters.

## RLC Overview

The RLC leverages the security and reliability of Rust, adding an industrial PLC's strict development and runtime environment. It uses TACL for logic program development and seeks to minimize the complexity between high-level logic and kernel-level code, offering developers flexibility to engage with both high-level IO logic and in-depth system programming. The project welcomes contributors who are eager to dive into both embedded and control systems programming within a singular platform.

## Innovation Over Imitation

We advocate for pioneering and original approaches rather than replicating established PLC functionalities. This project is as much an educational tool as it is a playground for innovation. It's about fostering inventiveness and expanding the community's skillset.

## Emphasis on Size

Our constraint is to prioritize compactness without compromising novelty. We focus on size over speed, given that the response time demands of PLC operations are comfortably within the capabilities of the underlying system. By staying close to the bare metal, we naturally enhance the RLC's speed, thereby affording us the luxury to optimize size without impacting logic performance.

## Design Requirements

### Target Architecture:

- Windows
- Linux
- Embedded Linux
- Bare metal embedded Rust

### Primary Controller Loop (PCL):

1. Housekeeping: Remote communications, accepting edits, etc.
2. Read Inputs
3. Evaluate and resolve logic
4. Set outputs

### Compilation:

The project supports piecemeal compilation of RLC programs, AOIs, UDTs, and similar elements to enable online edits.

We invite all interested parties to contribute to this novel undertaking, where your expertise can shine and influence the development of an open-source soft PLC platform that bridges Rust with the realm of industrial controls.