
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
```

![picorv32a](assets/screen3.png)
![Synthesis successful](assets/screen4.png)


flop ratio =(total no. of d flop realised) / (total no. cells)
           = 1613/14876
           = 0.10842


## Session 2: Good vs Bad Floorplanning

Run floorplan
```bash
% run_floorplan
```
![Floorplan Run](assets/screen5.png)
![Floorplan successful](assets/screen6.png)


#Calculate the Die area of the floorplan

# Change directory to path containing generated floorplan def
```bash
cd ~/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/04-10_15-44/tmp/floorplan
```
![Floorplan dir](assets/screen7.png)
![Floorplan def file](assets/screen8.png)


# Command to load the floorplan def in magic tool
```bash
magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.floorplan.def &
```
![Floorplan load def file](assets/screen9.png)

# Command to run placement
```bash
% placement
```
![Layout Magic](assets/screen10.png)
![Layout Magic](assets/screen11.png)


## Session 3: Designing Library Cell
## Session 4: Pre-Layout timing analysis
## Session 5: RTL2GDS using TritonROUTE and OpenSTA


