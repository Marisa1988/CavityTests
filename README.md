# CavityTests

Title: Cavity analysis of enzymes with MoloVol and its comparison with Deep View results. 
Author: Marisabel Morales

The data was obtained as part of the project AI-Driven Stabilization of Enzymes Treated Under High Hydrostatic Pressure, and can be accessed in GitHub repository: https://github.com/Marisa1988/CavityTests/tree/main

The research goal is to determine the effects of High Hydrostatic Pressure on enzyme structural conformation, focusing on the change in volume of buried cavities, to then integrate these findings into rational computational design of variants with increased thermostability.

This preliminary data was created to evaluate which algorithm may be the best option for detecting and analyzing internal cavities. The purpose of this data set is to compare specifically MoloVol and Deep View results.  

Input: This data set was digitally created using as input the experimentally determined 3D structures of enzymes obtained from the Protein Data Bank.

Parameters: The cavity detection was carried out with MoloVol, using a one-probe analysis with a radius of 1.4 Å and 0.47 Å of grid resolution, with the HETATM option disabled.

Output: The data output of MolVol includes the detected cavities, volume calculation and cavity detection of six oxidases (Alcohol Oxidase, Galactose Oxidase, Glucose Oxidase, L Amino Acid Oxidase, Oxalate Oxidase, and Xantine Oxidase) that are potentially relevant to the project and one small enzyme, lysozyme, which has been well characterized. 

Analysis: The visualization of the output was carried out with PyMol. A previous analysis was carried out with Deep View using a grid level of 6, equivalent to 0.47 Å. An image of the comparison of MoloVol and Deep View results is included.

Data organization: The data is currently organized in folders with the following structure:

1.	Enzyme name
  a.	Input
    i.	pdb file with the experimentally determined 3D structure. The Protein Data Bank uses a unique four-character alphanumeric code to identify each molecular model in its database. This code is called the PDB identifier or PDB ID.
  b.	Output
    i.	txt file that describes the surface and cavity calculation. MoloVol generates the complete report of the analysis, which includes the input, the parameters and the calculations for the total volume and the cavities. The name of the file includes a unique code for the calculation, the PDB ID, “MoloVol-report”, grid size and probe size.
    ii.	dx files of each detected cavity generated with MoloVol. The name of the file includes a unique code for the calculation, the PDB ID, grid size, probe size, and number of the cavity.
  c.	Analysis
    i.	pse file with the molecular analysis of cavities done with PyMol. The name of the file is the PDB ID_cavities.
    ii.	png file with the comparison of MoloVol and Deep View results. DeepView does not have the option to save or download the cavity analysis, which is why an image was used for this comparison.

The data was obtained on December 5th, 2024, and updated on January 13th, 2025. This preliminary data is part of an ongoing experiment. The next step is to run the same analysis with CASTpFold, a continuation of CASTp. 
