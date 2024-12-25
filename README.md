# Jonny's Custom KiCad Libraries
This repository contains my custom KiCad footprints and symbols.  
During various projects i am adding footprints for parts i could not find in the official library.  
Feel free to use them for your designs!


## Components Overview
Below is a list of components currently included in this library.  
Note: This list may not always be up-to-date or complete.
### Relays
        - LEG12 relay
        - Other small relays
#### ESP32 Development Boards
        - ESP32-DevKitV1 (30-pin) – e.g., Adafruit version
#### Connectors
        - 5mm screw terminals
          - 2-pin, 3-pin, and 4-pin variants
#### ICs
        - Custom footprints for specific ICs used in my projects



## Installation
1. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/Jonny999999/jonny-kicad-libs.git ~/git/kicad-library-jonny
   ```

2. Open KiCad (project manager) and add the library paths:
   - **Footprints:** Go to `Preferences > Manage Footprint Libraries > Global Libraries tab` and click `Add existing (Folder icon)`. Navigate to the cloned repository's `footprints/` directory and select all `.pretty` folders (Shift+Click)
   - **Symbols:** Go to `Preferences > Manage Symbol Libraries > Global Libraries tab` and click `Add existing (Folder icon)`. Navigate to the `symbols/` directory and add the desired `.lib` files.

3. Save your changes and start designing!


## Folder Structure
- `footprints/`: Contains all custom footprints organized by category.
- `symbols/`: Contains all custom symbols organized by category (multiple symbols in one .kicad_sym file).
