# APO-K2
**** SCROLL DOWN FOR UPDATES ****

Welcome to the companion GitHub to the APO-K2 Catalog Release. 

NB: The APO-K2 paper is current in submission and these numbers might be liable to change with improvements to the catalog. The current version of the PDF for the catalog can be found here: 
https://www.jessicastasik.com/_files/ugd/7c73a7_9cf838f60fe945e4b0342d8d4115c1f7.pdf

The selection function file contains its own README file describing how to use the selection function products. 

The publically available APO-K2 catalog is named in this directory as 'apo_k2_public_catalog.csv' and below is a detailed breakdown of each of the columns. 

| Column | Unit | Data Type | Description | 
|--------|------|-----------|-------------| 
| epic   | dimensionless | int | EPIC ID from the EPIC catalog. | 
| apogee | dimensionless | string | APOGEE ID from APOGEE DR17. | 
| gaia_source   | dimensionless | numpy | Gaia EDR3 source ID. | 
| camp   | dimensionless | string | Campaign number of the observation.[1] |
| ra     | degrees | float | Right Ascension from the EPIC catalog. | 
| dec    | degrees | float | Declination from the EPIC catalog. | 
| glat   | degrees | float | Galactic Latitude of the target. |
| glon   | degrees | float | Galactic Longitude of the target. | 
| ev     | dimensionless | string | The Evolutionary State of the target. | 
| teff   | kelvin | float | Calibrated effective temperature from APOGEE. | 
| teff_err | kelvin | float | Error on the APOGEE effective temperature. | 
| logg | dex | float | Calibratred surface gravity of target. | 
| logg_err | dex | float | Error on surface gravity. | 
| meh | dex | float | [M/H] from APOGEE. | 
| meh_err | dex | float | [M/H] error from APOGEE.| 
| feh | dex | float | [Fe/H] from APOGEE. |
| feh_err | dex | float | [Fe/H] error from APOGEE. | 
| alpham | dex | float | [Alpha/M] from APOGEE. | 
| alpham_err | dex | float | [Alpha/M] error from APOGEE.|
| alpha_flags | dimensionless | int | Flag depicting high- or low-alpha targets. [2]| 
| vmag | mag | float | V-band magnitude. | 
| vmag_err | mag | float | V-band magnitude error. | 
| jmag | mag | float | J-band magnitude. | 
| jmag_err | mag | float | J-band magnitude error. | 
| kmag | mag | float | K-band magnitude. |
| kmag_err | mag | float | K-band magnitude error. | 
| jk | mag | float | J-K color. | 
| j_k_err | mag | flat | J-K color error. |  
| numax | microhertz | float | Frequency of maximum oscillation power derived from K2 asteroseismology. | 
| numax_err | microhertz | float | Error on the frequency of maximum oscillation power derived from K2 asteroseismology. | 
| dnu | microhertz | float | Large frequency separation devived from K2 asteroseismology. | 
| dnu_err | microhertz | float | Error on the large frequency separation derived from K2 asteroseismology. | 
| fdnu | dimensionless | float | Large frequency correction. |
| fdnu_err | dimensionless | float | Error on the large frequency correction. | 
| fdnu_flags | dimensionless | float | Flag on fdnu. [3]| 
| kappa_m | dimensionless | float | Mass coefficient. | 
| kappa_m_err | dimensionless | float | Error on mass coefficient. | 
| mass | M$`{_\odot}`$ | float | Asteroseismically-derived mass. | 
| mass_err | M$`{_\odot}`$ | float | Error on mass. | 
| kappa_r | dimensionless | float | Radius coefficient. | 
| kappa_r_err | dimensionless | float | Error on radius coefficient. | 
| radius | R$`{_\odot}`$ | float | Asteroseismically-derived radius. | 
| radius_err | R$`{_\odot}`$ | float | Error on radius. | 
| para | mas | float | Corrected parallax from Gaia DR3. | 
| para_err | mas | float | Error on corrected parallax from Gaia DR3. | 
| ecc | dimensionless | float | Galactic eccentricity of the target. [4]| 
| ecc_err | dimensionless | float | Error on galactic eccentricity of the target. [4]| 
| zmax | kpc | float | Greatest distance of target from the Galactic plane during orbit. [4]| 
| zmax_err | kpc | float | Error on zmax [4]| 
| ang_mom | kpc km s$`^{-1}`$ | float | Angular momentum. [4]| 
| ang_mom_err | kpc km s$`^{-1}`$ | float | Error on angular momentum. [4]| 
| tot_energy | km$`^2`$ s$`^{-2}`$ | float | Total energy. [4]| 
| tot_energy_err | km$`^2`$ s$`^{-2}`$ | float | Error on total energy. [4]| 
| u    | km s$`^{-1}`$ | float | Positive velocity towards the Galactic center. [4]| 
| u_err | km s$`^{-1}`$ | float | Error on U. [4]| 
| v    | km s$`^{-1}`$ | float | Positive velocity towards the direction of Galactic rotation. [4]| 
| v_err | km s$`^{-1}`$ | float | Error on V. [4]| 
| w    | km s$`^{-1}`$ | float | Positive velocity towards the North Galactic Pole. [4]| 
| w_err | km s$`^{-1}`$ | float | Error on W. [4]| 
| gaia_binary_flag | numpy | float | Binary flag from Gaia DR3. [4]| 

[1] If this target was observed in multiple campaigns, these are contained in a list for the target's row.

[2] A value of 0 is $`\alpha`$-poor, and a value of 1 is $`\alpha`$-rich. Stars falling within $`2\sigma`$ of this ridge-line are given a value of -1. See [Warfield et al. (2024)](https://ui.adsabs.harvard.edu/abs/2024arXiv240316250W/abstract) 

[3] The second flag pertains to the $`f_{\Delta\nu}`$, where 0.0 corresponds $`f_{\Delta\nu}`$ value within the bounds of the grid and with a complete [Fe/H], the value is 1.0 if the value is computed by extrapolating beyond the bounds of the $`f_{\Delta\nu}`$ grid, and 2.0 if there is incomplete [Fe/H], T$`_{\mathrm{eff}}`$, $`\nu_{\mathrm{max}}`$, or $`\Delta\nu`$ information to compute $`f_{\Delta\nu}`$.

[4] For stars in these columns without data a float value of -999.0 is used and should be removed by the user. 

[5] This flag will be nonzero if either of the following are true: the star is flagged in the $`\texttt{non\_single\_star}`$ column of DR3 or the $`\texttt{fidelity\_v2}`$ value from Rybizki et al. (2022) (https://arxiv.org/abs/2101.11641) is $`\leq`$ 0.5 or unavailable.

For any questions, comments, or problems please contact the lead author Jessica Schonhut-Stasik at jessica.s.stasik@vanderbilt.edu.
Accessible text and other additional information can be found at https://www.jessicastasik.com/apo-k2.

**** UPDATES **** 

12.02.2024 -- New apo_k2_public_catalog.csv file uploaded to GitHub. Updated because roughly half of the previous Gaia DR3 source IDs were found to be incorrect. No other paramters were in error. 
