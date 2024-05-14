# Basis of Design

The RLC is intended to be a short stack, I.e. as few jumps as possible between, say, the kernel level code and the “high” level TACL. The programmer should want to use the RLC because it allows them both deep and shallow modification of an overall PLC-like control system. They can write the IO-facing top-level logic in a language that’s suited for it, and optimize or add to the core system programming in a more appropriate and powerful language. 

## Benefits

You’re not locked into a high level PLC language, but you’re also not stuck loading abstractions onto your firmware and software stack just to have a plc-like environment for the code that will change most often: that which modifies the IO.

You can work on embedded programming and controls programming on the same system.

## Constraints

As an Independent Constraint on the project I want to impose the challenge of making it as small as possible. As big as necessary, as big as the novelty requires, but focus on making it small too. Focus on size rather than speed, because the requires of the scan time of a PLC are much slower than the underlying system is capable of producing, which is good. So we will raise size slightly above speed. The closer we are to the bare metal, the faster the RLC be, and thus we can be slower and less optimized before impacting the logic executions.