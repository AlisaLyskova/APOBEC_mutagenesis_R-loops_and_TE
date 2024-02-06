# APOBEC_mutagenesis_R-loops_and_TE

This code is used for finding the mutation density (D_APOBEC) of the human APOBEC mutagenesis per target in R-loops and transposons.

Data with APOBEC mutations were obtained for 6 cancer types: BLCA, BRCA, CESC, HNSC, LUAD, LUSC. Files in directory data/APOBEC_mutated_position_cancer_samples have already been translated with liftOver to hg38 genome version. Links for downloading hg38 genome, R-loops coordinates and transposons coordinates are provided in jupyther notebook.

The first part is devoted to APOBEC mutagenesis in R-loops. First we search for potential APOBEC targets (TC) in and outside R-loops and count their number (N_TCN). Then we search for APOBEC-mutated targets in and outside R-loops (N_APOBEC) and calculate the mutation density D_APOBEC: D_APOBEC = N_APOBEC / N_TCN. The program for the second step was running separately as a python script in command line. The results file with the mutation density in R-loops by cancer type is located in data/outputs/D_APOBEC_RL.csv.

The second part is devoted to APOBEC mutagenesis in transposons. We studied the following groups of transposons: 'LINE', 'SINE', 'LTR', 'SVA', 'RC_transposons', 'DNA_transposons'. First we process transposons coordinates (we translated the coordinates to positive strand). Then we search for potential APOBEC targets and APOBEC-mutated targets in and outside transposons and calculate the mutation density D_APOBEC. This program was running separately as a python script in command line.
