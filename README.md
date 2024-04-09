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

![image](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/4693675b-37a7-4ee9-992b-6a4382e8e2a2)

![image](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/153d3001-cf54-4dc8-ae67-8ce1655db0d1)

![image](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/ef546b52-3044-4524-b06a-28042c646aec)

Based on the preceding outcomes, we can produce a floor plan that incorporates evenly spaced ports, equally spaced Decap and Tap cells. Following this placement, the standard cells are successfully positioned in compliance with legal placement rules.

# Day 3
## Design library cell using Magic Layout and ngspice characterization

![image](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/5eb1ac78-d0d5-4041-b309-0fef69f6fd4d)

![image](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/06525262-4f28-4b05-903a-8d24624af7d8)

![image](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/9ae15031-2fb7-428f-85ea-d95dafb4f777)

Today's lab covers the entire process of simulating an inverter using ngspice and the Magic EDA tool. Begin by changing to the specified directory to clone the necessary files from GitHub onto your local PC. Then, open a new terminal and navigate to this location. Copy the `sky130A.tech` file from its current location to the directory where you cloned the GitHub files. Finally, start up the Magic tool by initializing it in the terminal.

Inverter layout

![image](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/8ad0ab03-aa89-4a94-85d2-3a1ee9c53464)

nmos 

![image](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/c7acb6dd-595c-43ec-a6df-8e52fbc3ef8f)

pmos

![image](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/07c7e70f-a3bd-4efa-ab45-dd91b65b7b81)

Extract all the files

![image](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/f1161c99-4cd9-460f-9205-9d5c2c3e6550)

##  ngspice

To load spice file type the command - ngspice sky130_inv.spice followed by plot y vs time a

![image](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/4dc3f73b-90e8-4d85-b81f-9e71cba6c493)

Output

![image](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/35ea7375-b14d-4c90-b16e-842da6918e21)

Screenshot at 20%
![image](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/8e2ae89f-d2d2-49d7-b857-f3485adec976)

Screenshot at 80%
![image](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/76442d83-d19c-40cd-a4d8-04ce8507bd0e)

Rise time = 2.2464 - 2.1825 = 0.0639 ns = 63.9ps

Screenshot at 50% values of input and output
![image](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/2f986a19-920f-42fa-aa9e-121946ba722e)
Rise Cell Delay = 2.2121ns - 2.1516ns = 0.0605ns = 60.5ps

Screenshot at 50% values of input and output
![image](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/9f4e80b1-67a7-4025-b1c7-857c0f176fa1)
Fall Cell Delay = 4.077 - 4.050 = ns = 27ps

## Finding Errors in DRC by Magic tool

Sky130A Periphery rules: https://skywater-pdk.readthedocs.io/en/main/rules/periphery.html

 ![image](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/174e8a89-b6ca-4c71-b238-09fa0666360d)
 
To start magic, we use magic -d XR & for better display graphics using XR instead of the default X11. Using the GUI, click open to view the Met3.mag file in the viewer. As previously detailed, select a cell and in the TK console type cif see VIA2 to view the mask layer for via2, used in the final GDSII that is generated.

![image](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/6717a89a-6e00-487b-8670-8a44f51a97f3)



![image](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/e0eca2c9-83f3-4cb1-a049-cc82a8b2d1b9)

Change of Commands in sky130A.tech file

![image](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/2aaae403-a8fc-4fc9-b3ba-17bffb128b48)

Updating sky130A.tech file

![image](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/c4b2fbd2-997a-4884-be68-a20629773419)

![image](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/8d8cf024-5148-48ba-920d-c6c2baf58746)

the deep nwell is shown in the yellow stripes and the nwell is shown in dotted green pattern.

![image](https://github.com/SathvikAthreya/SoC_Design_and_Chip_Planning_Using_OpenLane/assets/165768197/26e78e96-ef35-45ed-984d-64718ba0cd61)

