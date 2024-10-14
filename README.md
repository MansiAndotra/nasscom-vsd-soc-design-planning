In this workshop, we will delve into the process of designing an Application Specific Integrated Circuit (ASIC) from the Register Transfer Level (RTL) to the Graphical Data System (GDS) using an open source tools "OPenLANE".
![image](https://github.com/user-attachments/assets/bd1a81ba-7746-4daf-8dbb-c4d35a13ed9f)
![image](https://github.com/user-attachments/assets/5e645a0f-1b74-44ae-9168-f44e83b0ba77)
Main Goal : To produce clean GDS II.
There are two modes to run the complete flow : Autonomus Mode { using .tcl where all commands required are written in script form } And Interactive Mode {step by step procedure }.

![image](https://github.com/user-attachments/assets/3e5a4948-56c0-4b15-94ab-e92aa62a2f5b)

![image](https://github.com/user-attachments/assets/abdfe047-0fe9-49af-9661-5b948f41a33b)
Openlane is our working directory. Envoke all tools in this directory.
To run in interactive mode (step by step mode): 
docker
bash-4.2$ ./flow.tcl -interactive
Package import and check
% package require openlane
Prepare design
To prepare and setup the design
% prep -design picorv32a
![image](https://github.com/user-attachments/assets/26efd091-bacc-4c80-adf9-24346ac53d63)
Once the preparation is complete, a new directory with the current date will be generated within the “runs” folder. Inside this directory, all the necessary subdirectories for storing results, reports, and other relevant data will be created.
![image](https://github.com/user-attachments/assets/bed847bb-64c2-47ec-9b27-76738cabdea7)
The preparation step involves the following actions for the picorv32a design within the openLANE flow:

Directory Structure Setup:

A new directory structure is created to organize the design files. This structure includes subdirectories for different components (e.g., results, reports).

LEF Merging: The technology LEF (.tlef) and cell LEF (.lef) files are merged into a unified format.The technology LEF contains layer information (such as metal layers), while the cell LEF contains cell informations.
Design Placement: All design-related files are placed under the designs directory. This ensures that the necessary files are organized and accessible during subsequent steps.
config.tcl	contains the configurations used by openLANE
src	contains verilog files and constraints file
this is merged.lef
![image](https://github.com/user-attachments/assets/c1b7aa1a-aae0-454c-acbe-82579e55dfab)

Synthesis % run_synthesis
![image](https://github.com/user-attachments/assets/4836e471-1ddb-4874-969a-54aad69cb4f9)
Calculating Clock Ratio : no. of d flip flop/ no. of cells = 1613/14876 = 0.1084296853993
![image](https://github.com/user-attachments/assets/68a28e79-aec5-45dc-ace1-05719740a98b)

![image](https://github.com/user-attachments/assets/912ece71-22bf-4b3c-b8bd-5e225d004b0f)
![image](https://github.com/user-attachments/assets/bce94577-6022-4f01-aebc-6742b29b2bbb)
![image](https://github.com/user-attachments/assets/7163dc96-ac4b-4857-bf25-f6686783024e)
placemnet 
![image](https://github.com/user-attachments/assets/9f85fad8-1048-430a-aab2-47b3393fd867)
![image](https://github.com/user-attachments/assets/07574949-373a-4748-8fb0-b6e270a35d79)

![image](https://github.com/user-attachments/assets/343ab449-3ddf-4798-9d35-7643cc15e057)
Github path for custom layout design flow
https://github.com/nickson-jose/vsdstdcelldesign

![image](https://github.com/user-attachments/assets/01c6e6e6-f637-41ad-b493-3a6a66d379a9)



