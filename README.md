# APO-K2
Welcome to the companion GitHub to the APO-K2 Catalog Release. 

NB: The APO-K2 paper is current in submission and these numbers might be liable to change with improvements to the catalog. The current version of the PDF for the catalog can be found here: 
https://www.jessicastasik.com/_files/ugd/7c73a7_9cf838f60fe945e4b0342d8d4115c1f7.pdf

The publically available APO-K2 catalog is named in this directory as 'apo_k2_public_catalog.csv' and below is a detailed breakdown of each of the columns. 

| Column | Unit | Data Type | Description | 
|--------|------|-----------|-------------| 
| epic   | dimensionless | int | EPIC ID from the EPIC catalog. | 
| apogee | dimensionless | string | APOGEE ID from APOGEE DR17. | 
| camp   | dimensionless | string | Campaign number of the observation.* |
| glat   | degrees | float | Galactic Latitude of the target. |
| glon   | degrees | float | Galactic Longitude of the target. | 
| ev     | dimensionless | string | The Evolutionary State of the target. | 
| teff   | kelvin | float | Effective temperature from APOGEE. | 
| teff_err | kelvin | float | Error on the APOGEE effective temperature. | 
| logg | dex | float | Surface gravity of target. | 
| logg_err | dex | float | Error on surface gravity. | 
| meh | dex | float | [M/H] from APOGEE. | 
| feh | dex | float | [Fe/H] from APOGEE. |
| alpham | dex | float | [Alpha/M] from APOGEE. | 
| vmag | mag | float | V-band magnitude. | 
| jk | mag | float | J-K color. | 
| numax | microhertz | float | Frequency of maximum oscillation power derived from K2 asteroseismology. | 
| dnu | microhertz | float | Large frequency separation devived from K2 asteroseismology. | 
| fdnu | dimensionless | float | Correction on large frequency separation. |
| kappa_m | dimensionless | float | Kappa coefficient for mass. | 
| mass | M_sun | float | Asteroseismically-derived mass. | 
| mass_err | M_sun | float | Error on mass. | 
| kappa_r | dimensionless | float | Kappa coefficient for radius. | 
| radius | R_sun | float | Asteroseismically-derived radius. | 
| radius_err | R_sun | float | Error on radius. | 
| ecc | dimensionless | float | Galactic eccentricity of the target. | 
| ang_mom | kpc km s^-1 | float | Angular momentum. | 
| tot_energy | km^2 s^-2 | float | Total energy. | 
| alpha_flag | dimensionless | int | Flag depicting high- or low-alpha targets. | 
| fdnu_flag | dimensionless | float | Flag on fdnu. | 

* If this target was observed in multiple campaigns, these are contained in a list for the target's row. 
For selection function data, please see the README in the file 'Selection Function' file. 

For any questions, comments, or problems please contact the lead author Jessica Schonhut-Stasik at jessica.s.stasik@vanderbilt.edu.
