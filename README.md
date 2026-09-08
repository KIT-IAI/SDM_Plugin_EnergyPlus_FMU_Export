# EnergyPlus FMU Export
The EnergyPlus FMU Export is a plugin for the [KITModelViewer](https://github.com/KIT-IAI/SDM_KITModelViewer) for exporting of CityGML EnergyADE building models as EnergyPlus Functional Mock-up Unit. 
Input for the plugin is a CityGML EnergyADE building model (see [EnergyADE Enrichment](https://github.com/KIT-IAI/SDM_Plugin_EnergyADE_Enrichment) for a enrichment plugin). Output is a fully self contained FMU, consisting of the building .idf file (Energy Plus input file), a .epw file (EnergyPlus weather) and the complete EnergyPlus simulator. 

## Highlights
- user-interface for FMU export
- multiple buildings and thermal zones supported
- FMU version 2.0 ready for co-simulation
- co-simulation with external HVAC system



<img width="977" height="787" alt="screenshot_gui" src="https://github.com/user-attachments/assets/aa99521c-af78-4084-babc-a9d6e55f4d2f" />


## Usage
- start with any CityGMl EnergyADE building model and goto Plugin -> create FMU
- select building and corresponding thermal zone and define in- and ouputs
- confirm settings by clicking "Apply to selected zones"
- select external weather data
- export FMU

Available FMU inputs:

| Group description    | Schedule name | Notes |
| -------- | ------- | ------- |
| IdealLoadsAirSystem | System Availability Schedule    | |
| IdealLoadsAirSystem | Cooling Availability Schedule   ||
| IdealLoadsAirSystem | Heating Availability Schedule   ||
| IdealLoadsAirSystem | Thermostat Heating Schedule   ||
| IdealLoadsAirSystem | Thermostat Cooling Schedule   ||
 | Internal Gains | Number of People Schedule   ||
 | Internal Gains | Lighting Power Schedule   ||
 | Internal Gains | Electric Equipment Schedule   ||
| External Equipment | Shading Controller Schedule   |creates a WindowShadingController Object|
 | External Equipment | Qconv   | convective sensible heating / cooling load, creates a OtherEquipment Object|
 | External Equipment | Qrad   |radiant heating / cooling load, creates a OtherEquipment Object|
 | External Equipment | Qlat   |latent heating / cooling load, creates a OtherEquipment Object|





For more information on these objects check the [EnergyPlus documentation](https://bigladdersoftware.com/epx/docs/23-1/).

## Examples
HVAC FMU, Shading Controller FMU

## Dependencies
coming soon

### Use of vcpkg:

|Package Name         |Install Command                            |
|:---                 |:---                                       |
|                     |vcpkg install --------- triplet=x64-windows|
|fmt                  |vcpkg install fmt triplet=x64-windows      |
|geographiclib 	      |vcpkg install geographiclib triplet=x64-windows|

## Literature
coming soon

## How to cite

```bibtex
@software{SDM_Plugin_EnergyPlus_FMU_Export,
	title        = {{SDM\_Plugin\_EnergyPlus\_FMU\_Export}},
	author       = {Steven Timothy Schuerstaedt},
	url          = {https://github.com/KIT-IAI/SDM_Plugin_EnergyPlus_FMU_Export},
	year         = {2026}
}
```






