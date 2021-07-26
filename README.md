# CubeSat-Mission-Planner
A Python-based tool to schedule satellite missions and simulate the resulting power behaviour. This tool was developed to help in the mission design of the [Da Vinci CubeSat](https://davincisatellite.nl/). As part of the mission design of this satellite, there existed a need to propagate a schedule of mission segments over time and verify the viability of such a schedule in terms of power behaviour. This tool facilitates such verification, although its accuracy is strongly dependent on the quality of the input data.

## Getting Started
To use this tool, clone this repository to a local directory, and open it in your coding editor of choice.
```
git clone https://github.com/Hans-Bananendans/CubeSat-Mission-Planner
```

## Prerequisites

### Python packages
To use the Satellite Mission Planner, a number of things are needed. This tool is coded in Python 3 and as such, Python 3 must be installed on your device, along with the following Python libraries:
 - 'NumPy'
 - 'MatPlotLib'
 - 'Time'
 - 'Pandas'
 
### Pre-formatted inputs
For successful simulation with this tool, it must be supplied with a number of pre-formatted inputs. More details will be given further on in this readme. A short overview of these inputs will be given here:
 - 'power.xlsx' contains a table with the power usage in *mW* broken down by subsystem and by OpState.
 - 'P_sun.npy' and 'P_alb.npy', two Numpy arrays containing the power input curves due to sunlight and albedo effect respectively. These curves can be generated by [CubeSat-Solar-Estimator](https://github.com/Hans-Bananendans/CubeSat-Solar-Estimator), another Python-based tool developed for the Da Vinci CubeSat project.
 - 'device_channels.py', a small file containing dicts that provide information about device channels.
 

## Nomenclature
### Custom Terms
 - **Channel**	-   A distinct power supply rail on the power distribution system. Many electrical power supply systems for satellites have several of such distinct rails, or "channels", to electrically isolate different devices on-board the satellite.
 - **Device**	-   Another name for a power-using subsystem on-board the satellite. A power user. For example: a cluster of sensors, a radio device, a payload system, etc.
 - **OpState** 	-   Short for Operational State. A discreet state of the satellite in which its power usage is constant. In the ideal case, the satellite's behaviour must be broken down into the smallest number of distinct OpStates. For example: a _Power Charging state_, an _Attitude Correction state_, etc.
 - **Schedule**	-   A schedule of satellite activity stating in which OpState the satellite should find itself at which point in time. For example: _At time t0, be in OpState A; at time t1, be in OpState B, etc..._

### Common Satellite-related Acronyms
 - **ADCS** -   Attitude Determination & Control System
 - **EPS**  -   Electrical Power System
 - **CDH**  -   Command & Data Handling
 - **LTAN** -   Local Time of Ascending Node
 - **OBC**  -   On-Board Computer
 - **RX**   -   Radio receiver
 - **TX**   -   Radio transmitter


## Software Layout
A functional layout of the tool's structure can be found below:
![alt text](./docs/layout.png?raw=true)

In a nutshell, the program asssembles a custom _Mission_ class, and uses 

## Usage


## Licence