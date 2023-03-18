Selection Function Documentation
-

This selection function directory contains four subdirectories, which contain the selection function data derived in the APO-K2 Catalog Paper 1. 
The file 'all_campaigns_together', contains the selection function tables when all data is considered as one catalog, the remaining four directories hold data for each of the selection function parameter spaces over all campaigns individually, so the user can see how the selection function changes over campaign. 

For the sake of this documentation, I explain use of the files in the all_campaigns_together directory, as the individual campaign files will work in the same way, and can be told apart by the addition to their filename of cX, where x corresponds to the campaign numbers (1-18, with the omission of 9). 

Inside the directory 'all_campaigns_together', there are four sub-directories, corresponding to the parameter space considered: mass_vs_radius, numax_vs_mag, color_vs_mag, and mass_vs_met. Each of these contains eight files, defined below: 

1. bin_edges_k2_sim.csv -- This list gives the x- and y-axis edges for the 10 x 10 grid into which the relative densities of the two samples are placed.
2. sim_density.csv -- This 10 x 10 grid contains the amount of stars that fall into each bin in the parameter space for the simulated data, with the bin edges given in file 1.
3. k2_density_(sim).csv -- This 10 x 10 grid contains the amount of stars that fall into each bin in the parameter space for the K2 observed data, with the bin edges given in file 1.
3. k2_sim_density.csv -- This 10 x 10 grid contains the relative number density of stars in each bin, with the bin edges corresponding to file 1. This relative density is the result of dividing file 3 by file 2 (i.e. K2 Observed Stars / Simulated Sample Stars). 

4. bin_edges_apok2_k2.csv -- This list gives the x- and y-axis edges for the 10 x 10 grid into which the relative densities of the two samples are placed. This file will not differ from file 1 because the parameters are pre-set but is output by the coding, the user can use either with no difference. 
5. apok2_density -- This 10 x 10 grid contains the amount of stars that fall into each bin in the parameter space for the APO-K2 data, with the bin edges given in file 1. 
6. k2_density_(apok2).csv -- This 10 x 10 grid contains the amount of stars that fall into each bin in the parameter space for the K2 observed data, with the bin edges given in file 1. NB: This file differs from k2_density_(sim) because in this second plot, the K2 observed stars are cut to the determined parameter space of the APO-K2 catalog, in order to populate the 10 x 10 bin within the limits provided. It will therefore contain less stars than the k2_density_(sim).csv and users wanting the full K2 observed sample should use file 3. 
7. apok2_k2_density.csv -- This 10 x 10 grid contains the relative number density of stars in each bin, with the bin edges corresponding to file 1. This relative density is the result of dividing file 6 by file 5 (i.e. APO-K2 Stars / K2 Observed Stars). 

Notes on recreating the Selection Function: 
-

* The plots that appear in the paper are scaled for the reader to clearly see changes in the relative amount of stars over the parameter space. However, these files are saved before any of this scaling takes place, in order to provide the user with the rawest data for their uses. The paper describes how scaling can be added. 
* All of the simulated stars are subject to a 0.1 multiplier. When the simulated sample was originally created, it was oversampled by around 10x. In order to give a more realistic representation of the full sample as it related to the observed samples, we multiple each of the bins in the simulated sample by 0.1. This will effect file 2 and 4 only.  

