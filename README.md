# MULTIFLOW_lava_flow_model README

Program description: the MULTIFLOW lava flow model performs flow routing on a digital elevation model (DEM) according to the multislope drainage routing algorithm. Multislope is the most laterally dispersive of flow routing algorithms, partitioning flow to all downslope cells in proportion to their local slope. A single calculation results in a map of 'influence', which MULTIFLOW then thresholds according to an empirical function to produce a flow of finite length. 

MULTIFLOW optionally allows for a pre-processing step of low-pass filtering the base DEM, which removes roughness elements with lateral wavelengths below the filter cutoff. When applied to mapped lava flow pathways from Kilauea, Mauna Loa, and Mt Etna volcanoes, it is found that filter cutoffs in the range of 50-270 m significantly improve the model fit. 

The manuscript "The multiscale influence of topogaphy on lava flow morphology" by Paul Richardson and Leif Karlstrom, currently accepted at Bulletin of Volcanology, details the choice of thresholds and spectral filtering.  

This code reproduces Figure 4a and c from Richardson and Karlstrom (2019), the influence and flow matching of the 1984 Mauna Loa lava flow in Hawaii, USA. Spectral filtering is performed on the pre-flow DEM to remove small roughness elements as a model for finite flow thickness. 

Copyright (C) 2019- Paul Richardson and Leif Karlstrom <leif@uoregon.edu>

This program is free software: you can redistribute it and/or modify it 
under the terms of the GNU General Public License as published by the 
Free Software Foundation. You should have received a copy of the GNU 
General Public License along with this program.  If not, see 
http://www.gnu.org/licenses.


### Included: 
- Matlab files for the MULTIFLOW code, including hillshade plotting functions and colormaps for plotting
- 10 m DEM of the Mauna Loa lava flow and background DEM

### Not included, but required dependencies:
- topotoolbox Matlab code, download from https://topotoolbox.wordpress.com/
- DEM spectral analysis tools from J. Taylor Perron (Massachusetts Institute of Technology), download from http://web.mit.edu/perron/www/downloads.html

### To run MULTIFLOW:
1. Download all code and data in this repository
2. Download topotoolbox and 2DSpecTools
3. execute the Matlab file MULTIFLOW_example_run.m








