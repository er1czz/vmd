# Instruction 1: use the Tcl script for VMD to calculate the amount of oil atoms on surface (within 0.36 nm)
1. Load the trajectory file in VMD; (e.g. wkpod300-comp.gro, drag the file to VMD Main or on **VMD Main** click **File** tab then **New Molecule ...**)
2. Open VMD TkConsole; (click **Extension** tab then **Tk Console**)
3. Set directory to the location of script file; (Use command "cd" and "cd .." to navigate and "pwd" to show current directory)
4. Type "source ott-count.txt" to execute the script;
5. The output will be generated as "cout_out.txt"

### Output file is formated as \<frame number> \<atom number>.
For example  
**0 0  
1 106  
2 198  
3 211  
4 213  
5 230**  

### File description:   
[**oct-count.txt**](https://er1czz.github.io/vmd/oct-count.txt): Tcl script to count numbers of non-polar oil atoms (resname OCT) within 3.6 Angstroms of kerogen surface (resname KER)   
[**ott-count.txt**](https://er1czz.github.io/vmd/ott-count.txt): Tcl script to count numbers of polar oil atoms (resname OTT) within 3.6 Angstroms of kerogen surface   
[**wkpod300-comp.gro**](https://er1czz.github.io/vmd/wkpod300-comp.gro): gromacs trajectory file (six frames) of a polar oil cluster (30 octanethiols) interaction with a kerogen surface

# Instruction 2: use the Tcl script for VMD to calculate the surface area of oil droplet (probing radius 0.14 nm)
Similar to instructuion 1.

### Output file is formated as \<frame number> \<total SA> \<water/oil contact area> \<surface/oil contact area>.
### unit: angstrom<sup>2</sup>  
For example  
**0 2889.4345703125 2848.1982421875 262.49859619140625  
1 3706.266357421875 2836.384033203125 975.4174194335938  
2 4283.4658203125 2657.725830078125 1629.1090087890625  
3 4248.119140625 2598.83251953125 1571.08984375  
4 4459.04833984375 2660.631103515625 1747.8780517578125  
5 4613.27392578125 2723.780517578125 1727.9306640625**

### File description:   
[**oct-sasa.txt**](https://er1czz.github.io/vmd/oct-sasa.txt): Tcl script to analyze surface area of non-polar oil droplet.   
[**ott-sasa.txt**](https://er1czz.github.io/vmd/ott-sasa.txt): Tcl script to analyze surface area of non-polar oil droplet.
