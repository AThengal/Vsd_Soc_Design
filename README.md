
# VSD-SOC-DESIGN-PROGRAM

## Description
Transforming bare RTL netlist to final tapeout

## Features
- Open Source Toolchain for RTL2GDS
- ASIC DESIGN FLOW

## Session 1: Open Source Tools
![Home screen](assets/screen1.png)

Open a shell inside the directory  ~/Desktop/work/tools/openlane_working_dir/openlane
![Application Screenshot](assets/screen2.png)

Run these commands
```bash
# Example of a command to install the project
docker
bash-4.2$ ./flow.tcl -interactive
% package require openlane
% prep -design picorv32a
% run_synthesis

![picorv32a](assets/screen3.png)
![Synthesis successful](assets/screen4.png)


flop ratio =(total no. of d flop realised) / (total no. cells)
           = 1613/14876
           = 0.10842


## Session 2: Good vs Bad Floorplanning
## Session 3: Designing Library Cell
## Session 4: Pre-Layout timing analysis
## Session 5: RTL2GDS using TritonROUTE and OpenSTA


