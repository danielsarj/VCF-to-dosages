# TOPMed-MESA-scripts

Python scripts to make dosage files without ambiguous SNPs and INDELs directly from `vcf.gz`. Both scripts essentially work the same, in which the outputs will be a sample `.txt` file (which is required to run PrediXcan) and a dosage `txt.gz` file per chromosome, including non-autosomes (if provided). The only difference is that `TOPMed_vcf2dosage_a.py` takes a `.vcf.gz` containg only a single chromosome as input, whereas `TOPMed_vcf2dosage_b.py` takes as input a `vcf.gz` containing multiple chromosomes. 

The scripts can also be customized if needed. As provided, they will rename all SNPs to the `chr#:pos:ref:alt` format and update chrX, chrXY, chrY, and chrM to their numeric versions.

Imported libraries:
* argparse
* gzip
* os
* sys

NOTE: this is a modified version of the script found in [here](https://github.com/WheelerLab/DivPop/blob/85100c2a41e2022e1e684e165980c3e9868db925/GWAS_QC/03_UMich_vcf2px_noambig_singlesnp.py).
