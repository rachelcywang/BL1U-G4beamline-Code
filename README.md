# Simulation Code for Beamline 1U at TRIUMF
Corresponding simulation code for work done on beamline 1U (BL1U) optimization at TRIUMF. Completed in part of an undergraduate thesis for the Combined Honours in Physics &amp; Astronomy program. A Monte Carlo simulation was performed on a G4beamline rendering of BL1U at TRIUMF in an effort to increase ultracold neutron production while avoiding target end window failure resulting from an excessive heat load. Simulation code for this project includes a .in file for G4beamline, FORTRAN code, Python code, and OPERA-3d modeller input file. The results of this thesis can be found in the UBC library.

*A few helpful notes:*
- For the G4beamline code: the input file into the simulation software must have a name of the form "MyG4InputFile.in"
- Regarding the FORTRAN file:
  - **Note: the input file must be named as "fort.1" and is obtained from OPERA-3d**
  - The fort.2 file must be in the same directory as the .in file
  - Some parameters must be changed on line 37/38 of the Opera2BLFieldMap.f file in accordance with the data table output parameters from OPERA-3d
  - The FORTRAN program may be run (using iFort) using the command line as such:
```
    > ifort Opera2BLFieldMap.f  # in the location of the .f file 
    > ./a.out  # returns output file called "fort.2"
```
- Provided Python code is for data extraction only
- SEPT.COMI file is the input file for the OPERA-3d modeller
