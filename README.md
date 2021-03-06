# MemSchedSim
This simulator models multi core systems, intended primarily for studies on
main memory management techniques. This simulator has been developed by many
people (Onur Mutlu, Yoongu Kim, Lavanya Subramanian) over time and has been
used for academic explorations of memory scheduling polices. It models a
trace-based out-of-order core frontend and models memory scheduling policies
such as FRFCFS, ATLAS, TCM, BLISS. It is not intended to be a perfect model of
all components of a multicore system. If you have any questions, you can raise
them and I will try to respond to them. However, since I have graduated and
moved on to other things, I will not be able to support the simulator and may
not respond to all questions/concerns.

To Compile:

make

The binary is created in the same folder.

To run:

Some sample command lines are available in the sample_command_line file

Trace files:

The trace file for each application consists of a stream of 12 byte records.
Each record is an 8-byte address memory address, followed by a 4-byte CPU
instruction count. The first bit of the address is borrowed to indicate load (0)
or store (1).

Simulator structure:

At a high level, the simulator is structured into the following directory
structure.

Sim: main simulator source, config and stats files
Proc: core and cache models
MemSched: different memory scheduler models
Mem: memory model
MemCtrl: memory controller model (modeling DRAM command timing)
