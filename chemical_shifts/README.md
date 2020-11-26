# Running the twister sister ribozyme 5Y87 using the FARFAR2 ROSIE server

We have supplied input files in this directory: the FASTA, the native (experimental) PDB structure, the secondary structure, and a STAR2.1 formatted file of chemical shifts. For simulation, upload these files to the corresponding inputs as directed in the text. To reproduce both runs that were compared in the text, simply omit the chemical shifts file.

# Interpreting the output

Because both simulations converge strongly on the "correct answer" and the question comes down to *how strongly* they converge, we supply constrained and unconstrained score files as a point of reference for output. (You may scatter plot the 'score' and 'rms' columns against each other to generate plots like those in the paper.) Those score plots are generated automatically by the ROSIE server itself for visualization.

To obtain the data necessary to make the same sort of plot yourself, you may go to the link "[Full set of decoy structures created on this run (FS view)]" or "[Download all job files as tar archive]" and look for the file "farna_rebuild.sc" if the native structure was provided as a reference during the run. If the native structure was not available, and you are interested in the score-versus-RMSD plot where the RMSD reference structure is the lowest energy structure created during the run, you can obtain the file "rescored.out," filter for only the lines beginning with "SCORE:" using a command line utility like grep, and plot that.