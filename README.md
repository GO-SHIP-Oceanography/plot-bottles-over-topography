# plot-bottles-over-topography

Code to plot CPD bottle depths over topography along a GO-SHIP transect.

Read in .btl and spit out bottle_schema_lonstart_lonend.png
To do that:

1. Download SRTM15_V2.3.nc or higher versions from https://topex.ucsd.edu/pub/srtm15_plus/ This is the gloabl geometry at 15 arcseconds (second link in https://topex.ucsd.edu/WWW_html/srtm15_plus.html). 
2. Run SRTM15_P02_extraction.ipynb to extract topography along the cruise track. 
3. Run P02w_bottle_plot.ipynb daily to generate daily bottle plots.

# Note

The code is not smart enough to directly read from the .btl file that CTD spits out. (see example file in ./btl_raw)
Instead, when I was at sea, I manually copied and pasted the data array from the .btl file and read that in matlab, and then took the depth column. 
This should and can be improved in the future code.

