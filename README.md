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
