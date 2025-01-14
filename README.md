# jonny's Custom KiCad Libraries
This repository contains my custom KiCad footprints and symbols.  
They were created during various projects for very specific needs or mostly for components not available in the official library.  
  
The repository serves as a centralized, version-controlled library, enabling reuse across multiple projects and devices.  


---


## Components Overview

Below is an overview of the components included in this library.  
_Note: This list may not always be up-to-date or complete._

| Category         | Component                             | Footprint Name                                  | 3D Model           | Details  |
|------------------|---------------------------------------|-------------------------------------------------|--------------------|-----------|
| **Relays**       | -                                     | -                                               | -  | -  |
|                  |                                       |                                                 |    |    |
| **Devboards**    | ESP32-DevKitV1 (30-pin)               | esp32-devkit-v1_30Pin                           | ![3d-model](images/3d-model_esp32-devkit-v1.jpg) | Custom symbol includes useful pin descriptions  ![ESP32-DevKitV1 Symbol](images/symbol_esp32-devkit-v1-30Pin.jpg) |
|                  |                                       |                                                 |    |    |

<br>

| Category         | Component                             | Footprint Name                                  | 3D Model           | Details  |
|------------------|---------------------------------------|-------------------------------------------------|--------------------|-----------|
| **Terminals**    | Screw Terminal 5mm Pitch (2-pin)      | ScrewTerminal_P5mm_2Pin_FP10x8                  | ![3d-model](images/3d-model_ScrewTerminal_P5mm-2Pin.jpg) | Footprint and 3d-model optimized for stacking terminals (Silk layer aligns and includes the actual key)|
|                  | Screw Terminal 5mm Pitch (3-pin)      | ScrewTerminal_P5mm_3Pin_FP15x8                  | ✅ | see above ^ |
|                  | Screw Terminal 2.5mm Pitch (WIP)      | -                                               | -  | Work in progress.  |
|                  | Hartmann Terminal 54191080051D, P2.5, 0.75mm2, 8-pole | Hartmann Terminal 54191080051D, P2.5, 0.75mm2, 8-pole - |  |
|                  | WAGO pinheader for connecting Terminals | WAGO 231-533 Print-Pinheader, Midi, P5.08, angled 3-pole  |  (✅)  |   |
|                  | WAGO pinheader for connecting Terminals | WAGO 713-1428 Pinheader double-deck MINI HD, P3.5, angled, 2x8-pole  |  (✅)  |   |
|                  | WAGO pinheader for connecting Terminals | WAGO 713-1430 Pinheader double-deck MINI HD, P3.5, angled, 2x10-pole |  (✅)  |   |
|                  | WAGO pinheader for connecting Terminals | WAGO 733-363 Print-Pinheader Micro, P2.5, angled 3-pole  |  (✅)  |   |
|                  | WAGO pinheader for connecting Terminals | WAGO 733-365 Print-Pinheader Micro, P2.5, angled, 5-pole |  (✅)  |   |
|                  | WAGO pinheader for connecting Terminals | WAGO 733-366 Print-Pinheader, Micro, P2.5, angled, 6-pole|  (✅)  |   |
|                  | WAGO pinheader for connecting Terminals | WAGO 734-162 Print-Pinheader, Mini, P3.5, angled, 2-pole |  (✅)  |   |
|                  | WAGO pinheader for connecting Terminals | WAGO 734-163 Print-Pinheader, Mini, P3.5, angled, 3-pole |  (✅)  |   |
|                  | WAGO pinheader for connecting Terminals | WAGO 734-164 Print-Pinheader, Mini, P3.5, angled, 4-pole |  (✅)  |   |
|                  | WAGO pinheader for connecting Terminals | WAGO 734-168 Print-Pinheader, Mini, P3.5, angled, 8-pole |  (✅)  |   |
|                  | WAGO pinheader for connecting Terminals | WAGO 736-306 double-deck-terminal, P5, 2.50mm2, 2x6-pole |  (✅)  |   |
|                  | WAGO pinheader for connecting Terminals | WAGO 736-308 double-deck-terminal, P5, 2.50mm2, 2x8-pole |  (✅)  |   |
|                  |                                       |  |    |   |

<br>

| Category         | Component                             | Footprint Name                                  | 3D Model           | Details  |
|------------------|---------------------------------------|-------------------------------------------------|--------------------|-----------|
| **ICs**          | -                                     | -                                               | -  | - |
|                  |                                       |                                                 |    |   |
| **Misc**         | Fuseholder Automotive Fuse "Regular"  | Fuseholder_Automotive-Regular_Fuse19x5x18mm     | -  |   |
|                  | Fuseholder Automotive Fuse "Mini"     | Fuseholder_Automotive-Mini_Fuse11x4x16          | ![3d-model](images/3d-model_Fuseholder-Automotive_Mini.jpg) |   |
|                  |                                       |                                                 |    |   |
| **Resistors**    | Cement 5W Power Resistor              | Cement-Power-R_L22_W10_P23_Horizontal           | -  | Minimal pitch footprint for horizontal placement.   |
|                  |                                       |                                                 |    |   |
| **Mounting Holes** | Custom mounting hole with NPTH      | MountingHole_2.2mm_NPTH-with-pad_DRC-clearance-error |    | NPTH with pads on both sides; good for mounting holes on GND planes, prevents having any clearance around the hole _(useful for fixation screws at PCB-milling)_ |
|                  | Custom mounting hole with NPTH        | MountingHole_2.2mm_NPTH-with-pad_DRC-shorts-nets|   |  see above ^     |



---
<br>


## Installation

#### 1. Clone the repository to your local machine:
```bash
# via SSH:
git clone git@github.com:Jonny999999/kicad-library-jonny.git ~/git/kicad-library-jonny
# or via HTTP:
git clone https://github.com/Jonny999999/jonny-kicad-libs.git ~/git/kicad-library-jonny
```

#### 2. [Optional] Get the Non-Public 3D Models
This project includes **3D models** collected from various sites for private use, those are stored in a separate private repository due to licensing restrictions.  
If you have access to that repo, clone it into the `3d-models/` folder:
```bash
cd 3d-models/
# via SSH:
git clone git@github.com:Jonny999999/kicad-library-jonny_nonPublicModels.git
# or via HTTP:
git clone https://github.com/Jonny999999/kicad-library-jonny_nonPublicModels.git
```
Without this step, all custom footprints in the library still work but a few corresponding 3d-models may be missing, which are nice to have, but optional for the pcb design.


#### 3. Open KiCad (project manager) and add the library paths:
- **Footprints:** 
  - Go to `Preferences > Manage Footprint Libraries > Global Libraries tab`
  - Click `Add existing (Folder icon)`. 
  - Navigate to the cloned repository's `footprints/` directory
  - Select all `.pretty` folders (Ctrl+Click to select multiple)  

- **Symbols:** 
  - Go to `Preferences > Manage Symbol Libraries > Global Libraries tab`
  - click `Add existing (Folder icon)`. 
  - Navigate to the `symbols/` directory 
  - Add the desired `.lib` files.

#### 4. Save changes by clicking `OK`

<img src="images/install_footprint-libraries.jpg" alt="Example Symbol" width="60%">

_Screenshot of Footprints installed_


---
<br>


## Usage

- Symbols are accessible as usual in the schematic-editor in the "Add Symbols" tool menu.
- Footprints can be assigned in the "Footprint Assignment Tool."
- **Note:** Most footprints currently lack custom symbols. Use generic symbols (e.g., Fuse or Screw Terminal) from the KiCad library in schematic-editor and manually map them in the assignment tool (`Tools` -> `Assign Footprints`),
- **Library Identification:** All custom libraries have `_libJonny` appended to explicitly distinguish them from standard libraries and to prevent any conflicts.


---
<br>


## Folder Structure
- [footprints/](footprints/): Contains all custom footprints organized by category.
- [symbols/](symbols/): Contains all custom symbols organized by category  
  __(Note: multiple symbols in one .kicad_sym file).__
- [3d-models/](3d-models/): Contains all custom 3d-models in `.step` plus original `.FCStd` format  
  (same folder structure and naming as in `footprints/` folder).

```bash
kicad-library-jonny
│   .gitignore
│   LICENSE
│   README.md
│
├───3d-models
│   ├───devboards
│   │       esp32-devkit-v1_30Pin.step
│   │
│   ├───kicad-library-jonny_nonPublicModels
│   ├───misc
│   │       Fuseholder_Automotive-Mini_Fuse11x4x16_Footprint15x5_Inline.FCStd
│   │       Fuseholder_Automotive-Mini_Fuse11x4x16_Footprint15x5_Inline.step
│   │
│   └───terminals
│           screw-terminals.FCStd
│           ScrewTerminal_P5mm_2Pin_FP10x8.step
│           ScrewTerminal_P5mm_3Pin_FP15x8.step
│
├───footprints
│   ├───devboards_libJonny.pretty
│   │       esp32-devkit-v1_30Pin.kicad_mod
│   │
│   ├───misc_libJonny.pretty
│   │       Fuseholder_Automotive-Mini_Fuse11x4x16_Footprint15x5_Inline.kicad_mod
│   │       Fuseholder_Automotive-Regular_Fuse19x5x18mm_Footprint21x8mm_Inline.kicad_mod
│   │
│   ├───mountingHoles_libJonny.pretty
│   │       MountingHole_2.2mm_NPTH-with-pad_DRC-clearance-error.kicad_mod
│   │       MountingHole_2.2mm_NPTH-with-pad_DRC-shorts-nets.kicad_mod
│   │
│   ├───resistors_libJonny.pretty
│   │       Cement-Power-R_L22_W10_P23_Horizontal.kicad_mod
│   │
│   └───terminals_libJonny.pretty
│           Hartmann Terminal 54191080051D, P2.5, 0.75mm2, 8-pole.kicad_mod
│           ScrewTerminal_P5mm_2Pin_FP10x8.kicad_mod
│           ScrewTerminal_P5mm_3Pin_FP15x8.kicad_mod
│           WAGO 231-533 Print-Pinheader, Midi, P5.08, angled 3-pole.kicad_mod
│           WAGO 713-1428 Pinheader double-deck MINI HD, P3.5, angled, 2x8-pole.kicad_mod
│           WAGO 713-1430 Pinheader double-deck MINI HD, P3.5, angled, 2x10-pole.kicad_mod
│           WAGO 733-363 Print-Pinheader Micro, P2.5, angled 3-pole.kicad_mod
│           WAGO 733-365 Print-Pinheader Micro, P2.5, angled, 5-pole.kicad_mod
│           WAGO 733-366 Print-Pinheader, Micro, P2.5, angled, 6-pole.kicad_mod
│           WAGO 734-162 Print-Pinheader, Mini, P3.5, angled, 2-pole.kicad_mod
│           WAGO 734-163 Print-Pinheader, Mini, P3.5, angled, 3-pole.kicad_mod
│           WAGO 734-164 Print-Pinheader, Mini, P3.5, angled, 4-pole.kicad_mod
│           WAGO 734-168 Print-Pinheader, Mini, P3.5, angled, 8-pole.kicad_mod
│           WAGO 736-306 double-deck-terminal, P5, 2.50mm2, 2x6-pole.kicad_mod
│           WAGO 736-308 double-deck-terminal, P5, 2.50mm2, 2x8-pole.kicad_mod
│
├───images
│
└───symbols
        devboards_libJonny.kicad_sym
        resistors_libJonny.bak
        resistors_libJonny.kicad_sym
        switches_libJonny.bak
        switches_libJonny.kicad_sym
```

---
<br>
