# Tutorial - use VMD Tcl/tk scripting to analyze a three-phase interface (water/oil/surface)
<img src="https://github.com/er1czz/vmd/blob/master/si%20illustration%20ab.jpg?raw=true" height="300" width="300">  

**Concept scheme: left, free droplet; right, adsorbed droplet.**  

## Example 1: calculate the amount of oil atoms on surface (within 0.36 nm)
### This calculation is based on the center-of-mass (COM) distance between the atoms of the oil molecules and the atoms of surface molecules.
0. Download VMD software https://www.ks.uiuc.edu/Research/vmd/  
1. Load the trajectory file in VMD; (e.g. wkpod300-comp.gro, drag the file to VMD Main or on **VMD Main** click **File** tab then **New Molecule ...**)
2. Open VMD TkConsole; (click **Extension** tab then **Tk Console**)
3. Set directory to the location of script file; (Use command "cd" and "cd .." to navigate and "pwd" to show current directory)
4. Type "source ott-count.txt" to execute the script and the data will be saved as "count_out.txt".  

#### Output file is formated as \<frame number> \<counts>. (delimited by space)
#### Output example  
**0 0  
1 106  
2 198  
3 211  
4 213  
5 230**  

### File description:   
[**oct-count.txt**](https://er1czz.github.io/vmd/oct-count.txt): Tcl script for counting numbers of non-polar oil atoms (resname OCT) within 3.6 Angstroms of kerogen surface (resname KER)   
[**ott-count.txt**](https://er1czz.github.io/vmd/ott-count.txt): Tcl script for counting numbers of polar oil atoms (resname OTT) within 3.6 Angstroms of kerogen surface   
[**wkpod300-comp.gro**](https://er1czz.github.io/vmd/wkpod300-comp.gro): gromacs trajectory file (six frames) of a polar oil cluster (30 octanethiols) interaction with a kerogen surface

## Example 2: calculate the surface area (SA) of oil droplet
### Solvent-accessible surface area method uses a imaginative sphere with a given probe radius (e.g. 0.14 nm) to measure the surface area of a selected region(s).
### <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d3/Accessible_surface.svg/280px-Accessible_surface.svg.png" height="240" width="196">  
Courtesy of Keith Callenberg from [Wikipedia](https://commons.wikimedia.org/wiki/File:Accessible_surface.svg)

0. Download VMD software https://www.ks.uiuc.edu/Research/vmd/  
1. Load the trajectory file in VMD; (e.g. wkpod300-comp.gro, drag the file to VMD Main or on **VMD Main** click **File** tab then **New Molecule ...**)
2. Open VMD TkConsole; (click **Extension** tab then **Tk Console**)
3. Set directory to the location of script file; (Use command "cd" and "cd .." to navigate and "pwd" to show current directory)
4. Type "source ott-sasa.txt" to execute the script and the data will be saved as "sasa_out.txt".  
  
#### Output file is formated as \<frame number> \<total SA of oil> \<contact SA of water/oil> \< contact SA of surface/oil>. (delimited by space)
#### Output example  
**0 2889.4345703125 2848.1982421875 262.49859619140625  
1 3706.266357421875 2836.384033203125 975.4174194335938  
2 4283.4658203125 2657.725830078125 1629.1090087890625  
3 4248.119140625 2598.83251953125 1571.08984375  
4 4459.04833984375 2660.631103515625 1747.8780517578125  
5 4613.27392578125 2723.780517578125 1727.9306640625**
#### unit: angstrom<sup>2</sup>  

### File description:   
[**oct-sasa.txt**](https://er1czz.github.io/vmd/oct-sasa.txt): Tcl script for analyzing surface area of a non-polar oil droplet.   
[**ott-sasa.txt**](https://er1czz.github.io/vmd/ott-sasa.txt): Tcl script for analyzing surface area of a polar oil droplet.    
[**wkpod300-comp.gro**](https://er1czz.github.io/vmd/wkpod300-comp.gro): gromacs trajectory file (six frames) of a polar oil cluster (30 octanethiols) interaction with a kerogen surface

## Reference  
arXiv preprint [https://arxiv.org/abs/2007.09741](https://arxiv.org/abs/2007.09741)  
Wikipedia [https://en.wikipedia.org/wiki/Accessible_surface_area](https://en.wikipedia.org/wiki/Accessible_surface_area)  
**>>>>>> [CC0 1.0 Public Domain Dedication](https://creativecommons.org/publicdomain/zero/1.0/) <<<<<<**  
You can copy, modify, distribute and perform the work, even for commercial purposes, all without asking permission. 
