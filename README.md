# Instruction: use the Tcl script for VMD to calculate number of oil atoms near surface
1. Load the trajectory file in VMD; (e.g. wkpod300-comp.gro, drag the file to VMD Main or on **VMD Main** click **File** tab then **New Molecule ...**)
2. Open VMD TkConsole; (click **Extension** tab then **Tk Console**)
3. Set directory to the location of script file; (Use command "cd" and "cd .." to navigate and "pwd" to show current directory)
4. Type "source ott-num.txt" to execute the script;
5. The output will be generated as "out.txt"

### Output file is formated as \<frame number> \<atom number>.
For example  
**0 0  
1 60  
2 103  
3 117  
4 119  
5 114**  

### File description:   
[**oct-num.txt**](https://er1czz.github.io/vmd/oct-num.txt): Tcl script to count numbers of non-polar oil atoms (resname OCT) within 3 Angstroms of kerogen surface (resname KER)   
[**ott-num.txt**](https://er1czz.github.io/vmd/ott-num.txt): Tcl script to count numbers of polar oil atoms (resname OTT) within 3 Angstroms of kerogen surface   
[**wkpod300-comp.gro**](https://er1czz.github.io/vmd/wkpod300-comp.gro): gromacs trajectory file (six frames) of a polar oil cluster (30 octanethiols) interaction with a kerogen surface
