# GeoStroke-Visualizer

An interactive web application for exploring driving-time-based accessibility to stroke care across Germany. This tool analyzes whether it may be clinically faster to transport stroke patients to the nearest CT-equipped hospital for immediate imaging and telestroke consultation, rather than direct transport to certified stroke units.

**🌐 [Access the Interactive Explorer](https://masannecklab.github.io/GeoStroke-Visualizer/)**

## The underlying analysis notebook can be found here: https://github.com/MasanneckLab/GeoStroke-Analyses 

## Publication

For detailed methodology and results, see:
Masanneck et al. (2025), "Direct stroke unit access versus a hub-and-spoke model with telemedicine-assisted CT in Germany: a cross-sectional geospatial analysis", *Lancet Regional Health Europe* (accepted). 10.1016/j.lanepe.2026.101604. - https://doi.org/10.1016/j.lanepe.2026.101604. 

## Features

### 📊 Dual Analysis Approach
- **Isochrone Analysis**: Visualizes accessibility to different types of stroke care facilities
- **Dual Benefit Analysis**: Compares direct transport vs. CT + telestroke strategy across multiple scenarios

### 🗺️ Geographic Coverage
- **State-level analysis**: All 16 German federal states
- **County-level analysis**: All 400+ German counties (Landkreise/Kreisfreie Städte)

### 🏥 Hospital Categories Analyzed
1. **CT-equipped hospitals**: Facilities with computed tomography capabilities
2. **Frequent stroke hospitals**: Facilities treating ≥100 stroke patients/year or certified stroke units
3. **Certified stroke units**: Specialized stroke treatment centers

### 🚗 Multiple Scenarios
- **Normal Speed**: Baseline driving conditions
- **+20% Emergency Speed**: Emergency vehicle privileges
- **-20% Traffic Speed**: Congested/adverse weather conditions
- **+10min Telestroke Penalty**: Remote consultation delay
- **+20min Telestroke Penalty**: Extended consultation time
- **+30min Telestroke Penalty**: Maximum consultation delay

## Data Downloads

### Scenario-Specific Data
- **Excel files**: Population and accessibility metrics for selected region/scenario
- **PDF reports**: Graphical representations for all regions in selected scenario

### Comprehensive Summaries
- **Excel summaries**: Cross-scenario statistics for all counties and states
- **PDF supplements**: Detailed tables comparing regular vs. extended analysis

## Repository Structure

```
docs/
├── index.html                          # Interactive web application
├── Results/
│   ├── Counties/                       # County-level analysis
│   │   ├── [State]/                    # Organized by federal state
│   │   │   ├── Isochrones_*.png        # Isochrone maps
│   │   │   └── pop_results_*.xlsx      # Population data
│   │   ├── Counties_CT_vs_Stroke_detailed.pdf
│   │   ├── County_Pop_Tables_CT_vs_Stroke.pdf
│   │   └── meta.json                   # County metadata
│   ├── States/                         # State-level analysis
│   │   ├── Isochrones_*.png            # State isochrone maps
│   │   ├── pop_results_*.xlsx          # State population data
│   │   └── meta.json                   # State metadata
│   └── Dual_All_Scenarios/             # Multi-scenario analysis
│       ├── [Scenario]/                 # Per-scenario results
│       │   ├── Counties/               # County dual benefit maps
│       │   └── States/                 # State dual benefit maps
│       ├── dual_benefit_*_stats_ALL.xlsx
│       ├── Supplement_*.pdf            # Comprehensive reports
│       └── pop_results_*.xlsx          # Detailed population data
```

## Usage

1. **Choose View**: Select between States or Counties
2. **Select Region**: Pick a state or county from the dropdown
3. **Explore Isochrones**: View accessibility maps for different hospital types
4. **Analyze Scenarios**: Use radio buttons to compare different conditions
5. **Download Data**: Access Excel files and PDF reports for detailed analysis

## Methodology

The analysis uses isochrone mapping to calculate driving times to different types of stroke care facilities. The dual benefit analysis compares two strategies:

1. **Direct transport** to nearest certified stroke unit or frequent stroke hospital
2. **CT + telestroke strategy** to nearest CT-equipped hospital with secondary transport if needed

Population-weighted accessibility metrics determine which regions would benefit from each approach under various scenarios.


## Technical Details

- **Built with**: Vanilla HTML/CSS/JavaScript
- **Hosting**: GitHub Pages
- **Data Format**: Excel/PNG files with JSON metadata
- **Browser Support**: Modern browsers with ES6 support

---

