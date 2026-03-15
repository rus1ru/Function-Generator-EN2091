# Function Generator (EN2091)

Hardware design repository for an analog function generator project, including PCB design sources, mechanical enclosure files, and project documentation.

## Project Overview

This repository contains the design artifacts for the EN2091 Function Generator project:

- Electronic design files (schematic and PCB layout)
- Mechanical enclosure and assembly CAD files
- Exported 3D models for integration and viewing
- Supporting documentation (datasheet, user manual, presentation)


Notes:
- The folder name Enclosuer Design Files is kept as-is to match the existing project structure.
- File naming is preserved from original design exports.

## Design Assets

### 1) PCB Design

Located in PCB Files:

- schematic_Func_Gen.SchDoc: Altium schematic source
- PCB_Func_Gen.PcbDoc: Altium PCB layout source

Use these files for circuit review, design updates, ERC/DRC checks, and fabrication export generation (Gerbers, drill files, BOM, pick-and-place).

### 2) Mechanical and Enclosure Design

Located in Enclosuer Design Files:

- Assembly New.SLDASM: Main SolidWorks assembly
- Box new.SLDPRT: Enclosure body part
- Box New Lid.SLDPRT: Enclosure lid part
- pcba.step: STEP export of the board assembly for mechanical fit checks
- knobs-15.snapshot.5/*.step: Knob variants as STEP files for integration

Use these files for enclosure modification, tolerance/fit validation, and 3D visualization.

### 3) Documentation

- Analog Function Generator Datasheet.pdf
- Analog Function Generator User Manual.pdf
- Analog Function Generator Presentation.pdf

These documents describe project intent, operation, and presentation material.

## Recommended Software

To work with the source files:

- Altium Designer (for .SchDoc and .PcbDoc)
- SolidWorks (for .SLDASM and .SLDPRT)
- Any CAD viewer with STEP support (for .step)
- PDF reader (for project documents)

## Getting Started

1. Clone the repository.
2. Open PCB Files/schematic_Func_Gen.SchDoc and PCB Files/PCB_Func_Gen.PcbDoc in Altium Designer.
3. Open Enclosuer Design Files/Assembly New.SLDASM in SolidWorks.
4. Verify PCB-to-enclosure fit using Enclosuer Design Files/pcba.step.
5. Review the Datasheet and User Manual before making design changes.


## License

This project is licensed under the MIT License.
See the LICENSE file for details.