# SoC_Design_and_Chip_Planning_Using_OpenLane_Flow_Report
#Design Flow Overview

Testbench in C: In ASIC design, a testbench is used to verify the functionality of the RTL design. It's typically written in HDL (like Verilog or VHDL) but can interface with C/C++ for higher-level control or complex test scenarios.
ASIC Design Flow: ASIC (Application-Specific Integrated Circuit) design involves a series of steps to create custom integrated circuits tailored for specific applications.
Specification and Architecture: Define the functionality, performance, and constraints of the ASIC.
RTL Design: Write the Register Transfer Level (RTL) description of the ASIC using hardware description languages (HDL) like Verilog or VHDL.
Functional Verification: Simulate the RTL code to ensure it behaves correctly according to the specification.
Synthesis: Convert the RTL description into a gate-level netlist using synthesis tools like Synopsys Design Compiler or Cadence Genus.
Floorplanning and Place-and-Route (PNR): Place the synthesized logic onto the physical chip layout, optimizing for performance, power, and area.
Static Timing Analysis (STA): Ensure that timing requirements are met across all paths in the design.
Physical Verification: Verify the physical design against manufacturing rules to ensure correctness and avoid manufacturing issues.
Design for Test (DFT): Insert testability features to facilitate manufacturing testing.
Signoff: Finalize the design and prepare for manufacturing.
RTL to GDS (RTL2GDS): This refers to the entire process of converting a Register Transfer Level (RTL) description of a circuit into a physical layout (GDSII format) that can be fabricated. It involves synthesis, PNR, and physical verification steps.
SOC Design Workshop: A System-on-Chip (SoC) design workshop focuses on the design and integration of complex systems onto a single chip. It covers topics ranging from architecture, RTL design, verification, and physical design.
Physical Verification: This is where the physical design is checked against design rules and constraints to ensure it can be manufactured correctly without issues like shorts, opens, or other layout-specific problems.
<img width="589" alt="Screenshot 2024-03-27 202140" src="https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/682f6375-b8bb-4a4d-8e67-1b080c30599d">

#Openlane Directory
