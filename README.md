This repository contains all of the supplementary data for the computational portion of the publication titled: 

Synthesis, biological activity, and molecular dynamics simulations of LNA-charge neutral linkages for enhanced splice-switching antisense oligonucleotides

#Alice Kennett, #Lillian Lie, Martin Flerin, Belma Zengin Kurt, Ysobel R. Baker, Alyssa C. Hill, Abinaya Ramesh, Matthew J.A. Wood, Debashis Dhara,Afaf H. El-Sagheer*, Fernanda Duarte* and Tom Brown*

# Files needed to run the simulations:
The folder Parameter_Files/md_parameters contains the parameters for the simulated annealing, equilibration and molecular dynamics runs. The Parameter_Files/additional_linker_paramers folder contains the gaff_params_bonded.itp and gaff_params_nonbonded.itp files, which contain all of the parameters which were added added to the original parm99 force field in order to simulate the modified linkers. The entire modified parm99.ff forcefield with the additional LNA parameters taken from Condon et al (J. Phys. Chem. B 2014, 118, 5, 1216–1228) and the neutral linkers obtained using GAFF in the Amber suite are found in the LNA_99_neutral.ff folder. Starting structures are located in the Parameter_Files/starting_structures folder. 

All other folders contain the raw data needed to produce Figure 2 in the main text, as well as all supplementary figures.

# Fig2A: 
This figure was generated using the representative structures of the 6 systems's combined trajectory files clustered using Chimera, using every 34th frame of the 30000 total frames, which are present as .pdb files in the folder most_populated_clusters. The structures of all of them were then visualised as ladders in Chimera, highlighting the two modified thymidines, whereas the inset zoomed in portion of the modified dithymidine was produced using Pymol. The population of the most populated cluster is shown in the brackets. 

# Fig2B: 
These curves of the combined trajectory RMSDs, which can be found in the RMSDs folder, were plotted as gaussian kernels usingthe scipy and matplotlib python libraries. The faint histogram in the background shows the distribution of the native control system's RMSDs split into 100 bins. 

# Fig2C: 
This plot of RMSF values across the different residues of the duplex was created using the data found in the RMSF folder. The values for the two nucleotides surrounding the locked linker in all of neutral linker-modified systems are the same for both the upstream and the downstream nucleotide, because they were parameterised as a single residue and are thus treated as such in the GROMACS rmsf calculation. 

# Fig2D: 
These figures were produced using dihedral angles around the central atom of each system's linker, by analysing the position of the most populated angles from all trajectories (distributions are shown in supplementary figure 21), teh raw data for which can be found in the dihedrals folder. The relevant atoms were extracted from the representative structures' .pdb files and visualised in Pymol.

# Fig2E: 
This plot was produced using the base pairing data output from the CPPTraj utility of AMBER, which has been concatenated for all runs and can be found in th H_bonding folder. The number of H-bonds for each residue was averaged, and the relative differences between the native system's inner 6 base pairs and the inner six base pairs of all other systems were plotted using the matplotlib library in Python.