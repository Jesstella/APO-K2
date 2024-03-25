# APO-K2 Ages

These are the full associated machine-readable tables from the second APO-K2 catalog paper (Warfield et al. 2024). They are:
- `t1_apok2_rgb_ages.txt`: Ages for stars classified as RGB in the APO-K2 catalog.
- `t2_apokasc2_rgb_ages.txt`: Ages for stars classified as RGB in the APOKASC2 catalog.
- `t3_apok2_rc_ages.txt`: Ages for stars classified as RC in the APO-K2 catalog. These ages are calculated using the asteroseismic masses of these stars with no prescription for mass loss, and should be used with extreme caution and care.
- `t4_apok2_lowfeh_ages.txt`: Ages for stars in the APO-K2 catalog with [Fe/H] < -1.
The headers of each file (which can be read using a normal text editor) describe the available columns and units.

One of the easiest ways to read these files in in a `Python` script is to use `astropy`:
```
from astropy.io import ascii

table = ascii.read(filename) # astropy table object
df = table.to_pandas()       # as a pandas DataFrame
```
