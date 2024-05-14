# Design Requirements

## API requirements

1. Example program code file (`main.tacl`)
2. Example data code file (`data.tacl`)
3. Sample local IO code file (`local_io.tacl`)
4. Example remote IO code file (`remote_io.tacl`)
5. Example controller code file (`controller.tacl`)

## Target architecture

1. Windows
2. Linux
3. embedded Linux
4. bare metal embedded Rust

## Primary Controller Loop (PCL)

The Primary Control Loop is the global loop and order of operations of the RLC. It follows the design of traditional PLCs and deviates as needed.

1. Housekeeping
    1. Remote Communications
    2. Accepting edits, applying configuration changes
    3. Setting programs on and off scan
    4. Etc.
2. Read Inputs
3. Evaluate and resolve logic
4. Set outputs

## Execution Control

1. Piecemeal compilation of RLC programs, AOIs, UDTs, etc. In essence, the parts that allow us to perform online edits and enable/disable execution of particular programs and structures.