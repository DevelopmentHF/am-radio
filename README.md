# AM Radio

A custom analog AM radio project designed to explore practical RF, analog electronics, PCB and mechanical enclosure design.

The project will cover the full signal chain, including:

- AM antenna and RF front end
- Tuning and filtering
- Superheterodyne frequency conversion
- IF filtering and amplification
- AM demodulation
- Audio amplification
- Speaker output
- LTspice simulation
- KiCad schematic and PCB design
- CAD enclosure and mechanical integration

The aim is to document the design process from requirements and simulations through to a working physical radio.

## Tools

- KiCad
- LTspice
- Fusion360

## Status

Work in progress.

## Project Structure

```
am-radio/
├── docs/                  # Design documentation and engineering rationale
│   ├── calculations/      # Design calculations and component sizing
│   ├── decisions/         # Design decisions and trade-off records
│   └── references/        # Datasheets, app notes, books, and useful links
├── hardware/              # Physical implementation of the radio
│   ├── antenna/           # Antenna design, measurements, and construction notes
│   ├── cad/               # Enclosure and mechanical CAD files
│   └── pcb/               # KiCad schematic and PCB design
├── images/                # Schematics, renders, plots, and prototype photos
├── sims/                  # LTspice simulations and simulation models
└── test/                  # Verification and validation
    ├── real/              # Physical hardware measurements and test results
    └── sims/              # Simulation-based test and verification results
```