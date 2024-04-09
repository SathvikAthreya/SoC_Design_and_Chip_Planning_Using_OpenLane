# SoC_Design_and_Chip_Planning_Using_OpenLane_Flow_Report
# Day 1
-----
## Design Flow Overview

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

## Openlane Directory

![Screenshot 2024-04-03 110119](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/fbf41c74-0b66-414e-8828-c5dd047599a0)

## To open the Openlane

![Screenshot 2024-04-03 112134](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/69046fea-1e58-4722-a2a1-c3854a15d1cf)

## To run the Synthesis

![Screenshot 2024-04-09 194526](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/4f0269ce-fdd9-4aa7-a372-bd9277eaafc8)

## Calculating Flop Ratio

![Screenshot 2024-04-03 124809](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/5cddb022-96be-4d51-9a2e-c3d43263093d)

Number of cells: 14876
Number of FF: 1613

         Flop ratio in (%) = Total No of D-FF
                           --------------------  X 100
                            Total No of Cells
                            
                          = 1613
                          --------   X 100
                            14876 

                          = 10.8429685
                          
# Day 2
## Florplan and Placement Stage

After running the floor plan command 

![image](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/4b955c8f-aaa4-4c27-8af4-712cbc054464)

![image](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/4aa3ef4f-7f0b-4177-8ed9-285b0fbc207b)

1000 unit distance = 1 Micron
Distance in micron =                  value
                                     ----------
                                      1000

 Die width in micron =                    660685 
                                         ---------
                                          1000
                            
 Die height in micron =                     671405 
                                           ---------
                                             1000

the width of chip is 660.685 micrometer and height of the chip is 671.405 micrometer.

![image](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/225b88eb-8cb7-44aa-88c2-27cf7879443d)


