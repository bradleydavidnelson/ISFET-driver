# ISFET-driver
>Adjustable driver circuit for ISFET sensing.

---
## Table of Contents
1. [Getting Started](#getting-started)
1. [Usage](#usage)
1. [Troubleshooting](#troubleshooting)
1. [Contributors](#contributors)
1. [License](#license)

---
## Getting Started
The board design consists of 2 Eagle boards:
- `ChemFET Multi` handles power management and contains adjustable voltage levels for V<sub>ds</sub>, V<sub>ref</sub>, and V<sub>offset</sub>. Inputs are available for 4 pairs of ISFET connections (source and drain) and the reference electrode. Outputs are available for 4 voltage readouts and ground level. Power may be supplied either via micro USB, or by screw terminals with an additional wire for enable/disable. 4 sets of board to board headers are available to connect to the SD follower breakout boards.
- `ChemFET SD Follower Breakout` handles the signal transduction from the ISFET to voltage output corresponding to ion level in solution. This design uses a source-drain follower circuit which implements an instrumentation amplifier with the ISFET acting as the gain resistor.

---
## Usage
The onboard potentiometers allow several adjustable voltages:
- V<sub>ds</sub>: Between 0 and 1 V
- V<sub>ref</sub>: Between 0 and 5 V
- V<sub>offet</sub>: between -5 and 5 V

For the nitrate FETs: Vds is set at 0.3 V. Vref is set at 1.5 V so that the FET operates in the linear mode. Voffset is set at 0 V, but may be adjusted if the voltages are near the edge of the measurement range. To set these voltages, attach a voltmeter or multimeter to the test relevant test points and adjust the potentiometers when the circuit is powered on.

---
## Troubleshooting

---
## Contributors
- Brad Nelson (https://github.com/bradleydavidnelson)

---
## License
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
