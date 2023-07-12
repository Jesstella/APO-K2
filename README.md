# APO-K2
Welcome to the companion GitHub to the APO-K2 Catalog Release. 

NB: The APO-K2 paper is current in submission and these numbers might be liable to change with improvements to the catalog. The current version of the PDF for the catalog can be found here: 
https://www.jessicastasik.com/_files/ugd/7c73a7_9cf838f60fe945e4b0342d8d4115c1f7.pdf

The selection function file contains its own readme file describing how to use the selection function products. 

The publically available APO-K2 catalog is named in this directory as 'apo_k2_public_catalog.csv' and below is a detailed breakdown of each of the columns. 

| Column | Unit | Data Type | Description | 
|--------|------|-----------|-------------| 
| epic   | dimensionless | int | EPIC ID from the EPIC catalog. | 
| apogee | dimensionless | string | APOGEE ID from APOGEE DR17. | 
| gaia   | dimensionless | numpy | Gaia EDR3 source ID. | 
| camp   | dimensionless | string | Campaign number of the observation.[1] |
| glat   | degrees | float | Galactic Latitude of the target. |
| glon   | degrees | float | Galactic Longitude of the target. | 
| ev     | dimensionless | string | The Evolutionary State of the target. | 
| teff   | kelvin | float | Effective temperature from APOGEE. | 
| teff_err | kelvin | float | Error on the APOGEE effective temperature. | 
| logg | dex | float | Surface gravity of target. | 
| logg_err | dex | float | Error on surface gravity. | 
| meh | dex | float | [M/H] from APOGEE. | 
| meh_err | dex | float | [M/H] error from APOGEE.| 
| feh | dex | float | [Fe/H] from APOGEE. |
| feh_err | dex | float | [Fe/H] error from APOGEE. | 
| alpham | dex | float | [Alpha/M] from APOGEE. | 
| alpham_err | dex | float | [Alpha/M] error from APOGEE.]
| alpha_flag | dimensionless | int | Flag depicting high- or low-alpha targets. | 
| vmag | mag | float | V-band magnitude. | 
| vmag_err | mag | float | V-band magnitude error. | 
| jmag | mag | float | J-band magnitude. | 
| jmag_err | mag | float | J-band magnitude error. | 
| jk | mag | float | J-K color. | 
| j_k_err | mag | flat | J-K color error. |  
| numax | microhertz | float | Frequency of maximum oscillation power derived from K2 asteroseismology. | 
| numax_err | microhertz | float | Error on the frequency of maximum oscillation power derived from K2 asteroseismology. | 
| dnu | microhertz | float | Large frequency separation devived from K2 asteroseismology. | 
| dnu_err | microhertz | float | Error on the large frequency separation derived from K2 asteroseismology. | 
| fdnu | dimensionless | float | Large frequency correction. |
| fdnu_err | dimensionless | float | Error on the large frequency correction. | 
| fdnu_flag | dimensionless | float | Flag on fdnu. | 
| kappa_m | dimensionless | float | Mass coefficient. | 
| kappa_m_err | dimensionless | float | Error on mass coefficient. | 
| mass | M_sun | float | Asteroseismically-derived mass. | 
| mass_err | M_sun | float | Error on mass. | 
| kappa_r | dimensionless | float | Radius coefficient. | 
| kappa_r_err | dimensionless | float | Error on radius coefficient. | 
| radius | R_sun | float | Asteroseismically-derived radius. | 
| radius_err | R_sun | float | Error on radius. | 
| para | mas | float | Corrected parallax from Gaia DR3. | 
| para_err | mas | float | Error on corrected parallax from Gaia DR3. | 
| ecc | dimensionless | float | Galactic eccentricity of the target. | 
| ecc_err | dimensionless | float | Error on galactic eccentricity of the target. | 
| ang_mom | kpc km s^-1 | float | Angular momentum. | 
| ang_mom_err | kpc km s^-1 | float | Error on angular momentum. | 
| tot_energy | km^2 s^-2 | float | Total energy. | 
| tot_energy_err | km^2 s^-2 | float | Error on total energy. | 
| gaia_binary_flag | numpy | float | Binary flag from Gaia DR3. | 

[1] If this target was observed in multiple campaigns, these are contained in a list for the target's row. 
For selection function data, please see the README in the file 'Selection Function' file. 

For any questions, comments, or problems please contact the lead author Jessica Schonhut-Stasik at jessica.s.stasik@vanderbilt.edu.
Accessible text and other additional information can be found at https://www.jessicastasik.com/apo-k2.
