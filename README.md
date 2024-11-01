# Impact and Management of Grid-Connected Energy Storage Systems

This project investigates the role of Battery Energy Storage Systems (BESS) in stabilizing grid-connected power systems with high photovoltaic (PV) penetration. The analysis focuses on voltage support, frequency stability, and power transfer capacity through simulations in DIgSILENT PowerFactory.

## Project Overview

### Objectives
The primary goals of this project are to:
- **Voltage Support**: Analyze BESS capabilities for voltage stability through reactive power support.
- **Frequency Stability**: Examine how BESS integration enhances frequency stability by providing synthetic inertia to reduce frequency deviations.
- **Transmission Capacity**: Evaluate BESS impact on transmission line capacity, with emphasis on congestion relief and power transfer efficiency.
- **Solar Irradiance Influence**: Study the effect of varying solar irradiance on PV generation and overall grid stability.

### Methodology
This project uses a single "Base Case" in DIgSILENT PowerFactory, which was modified manually to create various simulation scenarios:
- **EMT Simulations**: Generated electrical frequency curve plots to assess frequency stability.
- **Quasi-Dynamic Simulations**: Produced active power plots at the NW-Central 400 kV transmission line to analyze power flow and system stability.

## Repository Structure

```
├── data/
│   ├── solar irradiance data           # Solar irradiance data for PV generation simulation
│   ├── Load Demand.xlsx              # Load profile data for the 21-bus system
│  
├── model/
│   └── MTTFRA005_21 Bus System.pfd        # DIgSILENT PowerFactory model file for the 21-bus system
├── results/
│   ├── EMT Simulations  # EMT simulation frequency response plots folder with screenshots of results
│   ├── Quasi Dynamic Simulations  # Screenshots of quasi dynamic plots
│   └── BESS Tuning best results     
└── README.md
```

## Usage

### Prerequisites
- **DIgSILENT PowerFactory**: Required to run .pfd model files
- **Python 3.9.2**: Needed for running data analysis scripts

### Running Simulations
1. **Open Base Case**: Load `powerfactory_model.pfd` in DIgSILENT PowerFactory.
2. **Manual Parameter Variation**: Adjust parameters within the Base Case model to simulate different scenarios, such as:
   - **EMT Simulations**: Frequency response under load variations.
   - **Quasi-Dynamic Simulations**: Power flow on the NW-Central 400 kV line.
3. **Analyze Results**: Use the plots and data saved in the `results/` folder to interpret the effects of BESS on system stability.

### Data Processing
- Solar irradiance and load profile data are available in the `data/` directory.
- System configuration parameters can be edited in `parameters.yaml`.

## Results Overview

### Voltage Stability
The BESS significantly improved voltage stability, especially in high PV penetration scenarios, as observed in FVSI analysis.

### Frequency Stability
Synthetic inertia from BESS helped stabilize frequency fluctuations, contributing to better frequency response during sudden load changes. System still has instability though.

### Transmission Capacity
BESS integration enhanced transmission capacity, reducing congestion and stabilizing power flow under peak demand conditions.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments
- Thanks to Dr David Oyedokun for guidance on stability analysis.
- Resources: Solar irradiance data sourced from PVGIS.com.
