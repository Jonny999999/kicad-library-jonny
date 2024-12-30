# jonny's Custom KiCad Libraries
This repository contains my custom KiCad footprints and symbols.  
During various projects i am adding footprints for parts i could not find in the official library.  

---

## Components Overview
Below is a list of components currently included in this library.  
Note: This list may not always be up-to-date or complete.

### Relays

### Devboards
- **ESP32-DevKitV1 (30-pin)** – e.g. Adafruit version
    - _Name:_ esp32-devkit-v1_30Pin
    - _Symbol:_ custom symbol includes **detailed pin descriptions**
    - _3d-model:_ includes 3d-model
        
### Terminals
- **ScrewTerminal 5mm Pitch** very common (usually blue)
    - _Name:_ ScrewTerminal_P5mm_2Pin_FP10x8 + custom 3d-model
    - _Name:_ ScrewTerminal_P5mm_3Pin_FP15x8 + custom 3d-model
    - _3d-model:_ custom 3d-model + FreeCAD file
    - _Note:_ Footprint and 3d-model include details for optimal arrangement to stack multiple terminals
- **ScrewTerminal 2.5mm Pitch** very common (usually blue) WIP

### ICs

### Misc
- **Fuseholder Automotive Fuse "Regular"**
    - _Name:_ Fuseholder_Automotive-Regular_Fuse19x5x18mm_Footprint21x8mm_Inline
- **Fuseholder Automotive Fuse "Mini"**
    - _Name:_ Fuseholder_Automotive-Mini_Fuse11x4x16_Footprint15x5_Inline
    - _3d-model:_ custom 3d-model + FreeCAD file

### Resistors
- **Cement 5W power resistor**
    - _Name:_ Cement-Power-R_L22_W10_P23_Horizontal
    - _Note:_ minimal pitch footprint

### MountingHoles
- custom mounting **hole footprints with NPTH plus pads** on front and back copper.  
  Idea:
    - have mountholes on GND planes without any isolation areas
    - use NPTH to have those holes export to a separate drillfile -> mill those first to fixate pcb with screws
    - note: causes DRC errors that have to be ignored (no workaround found)


<br>

---

<br>

## Installation
1. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/Jonny999999/jonny-kicad-libs.git ~/git/kicad-library-jonny
   ```

2. Open KiCad (project manager) and add the library paths:
   - **Footprints:** Go to `Preferences > Manage Footprint Libraries > Global Libraries tab` and click `Add existing (Folder icon)`. Navigate to the cloned repository's `footprints/` directory and select all `.pretty` folders (Ctrl+Click)
   - **Symbols:** Go to `Preferences > Manage Symbol Libraries > Global Libraries tab` and click `Add existing (Folder icon)`. Navigate to the `symbols/` directory and add the desired `.lib` files.

3. Save changes

<br>

---

<br>

## Usage
- The symbols are included in the usual "Add Symbols" tool menu
- The footprints are included in the "footprint assignment tool"
- Note: Currently most footprints do not have a custom symbol, so use a generic symbol (e.g. Fuse or screwTerminal) from the kicad library and then in the footprint assignment tool manually select / map it to the desired custom footprint
- Note: all footprint and symbol libraries have `_libJonny` appended, so it is clear when using standard or custom footprints

<br>

---

<br>

## Folder Structure
- [footprints/](footprints/): Contains all custom footprints organized by category.
- [symbols/](symbols/): Contains all custom symbols organized by category  
  (Note: multiple symbols in one .kicad_sym file).
- [3d-models/](3d-models/): Contains all custom 3d-models in `.step` plus original `.FCStd` format  
  (same folder structure and naming as in `footprints/` folder).


```bash
kicad-library-jonny
├── 3d-models
│   ├── devboards
│   │   └── esp32-devkit-v1_30Pin.step
│   ├── misc
│   │   ├── Fuseholder_Automotive-Mini_Fuse11x4x16_Footprint15x5_Inline.20241228-110455.FCBak
│   │   ├── Fuseholder_Automotive-Mini_Fuse11x4x16_Footprint15x5_Inline.FCStd
│   │   └── Fuseholder_Automotive-Mini_Fuse11x4x16_Footprint15x5_Inline.step
│   └── terminals
│       ├── ScrewTerminal_P5mm_2Pin_FP10x8.step
│       ├── ScrewTerminal_P5mm_3Pin_FP15x8.step
│       ├── screw-terminals.20241228-134231.FCBak
│       └── screw-terminals.FCStd
├── footprints
│   ├── devboards_libJonny.pretty
│   │   └── esp32-devkit-v1_30Pin.kicad_mod
│   ├── ics_libJonny.pretty
│   ├── misc_libJonny.pretty
│   │   ├── Fuseholder_Automotive-Mini_Fuse11x4x16_Footprint15x5_Inline.kicad_mod
│   │   └── Fuseholder_Automotive-Regular_Fuse19x5x18mm_Footprint21x8mm_Inline.kicad_mod
│   ├── mountingHoles_libJonny.pretty
│   │   ├── MountingHole_2.2mm_NPTH-with-pad_DRC-clearance-error.kicad_mod
│   │   └── MountingHole_2.2mm_NPTH-with-pad_DRC-shorts-nets.kicad_mod
│   ├── relays_libJonny.pretty
│   ├── resistors_libJonny.pretty
│   │   └── Cement-Power-R_L22_W10_P23_Horizontal.kicad_mod
│   └── terminals_libJonny.pretty
│       ├── ScrewTerminal_P5mm_2Pin_FP10x8.kicad_mod
│       └── ScrewTerminal_P5mm_3Pin_FP15x8.kicad_mod
├── README.md
└── symbols
    ├── devboards_libJonny.bak
    └── devboards_libJonny.kicad_sym

14 directories, 19 files
```
