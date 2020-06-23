# Instruction: use the Tcl script for VMD to calculate number of oil atoms within 3 Angstroms of kerogen surface
1. Load the trajectory file in VMD; (e.g. wkpod300-comp.gro, drag the file to VMD Main or on **VMD Main** click **File** tab then **New Molecule ...**)
2. Open VMD TkConsole; (click **Extension** tab then **Tk Console**)
3. Set directory to the location of script file; (Use command "cd" and "cd .." to navigate and "pwd" to show current directory)
4. Type "source ott-num.txt" to execute the script; (ott-num.txt for counting polar oil and oct-num.txt for counting non-polar oil)
5. The output will be generated as "out.txt"

### Output file is formated as \<frame number> \<atom number>.
<br /> example output 
<br /> 0 0 
- 1 60
- 2 103
- 3 117
- 4 119
- 5 114

