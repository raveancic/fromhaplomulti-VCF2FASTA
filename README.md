# From haploid multiVCF 2 FASTA

This repo contains a jupyter [notebook](https://github.com/raveancic/fromhaplomulti-VCF2FASTA/blob/main/fromVCF2FASTABeastReport.ipynb) usefull to convert an haploid multi-vcf to a multi-FASTA file. Ready to be imported in other software and perform other analyses. 
This script exploits many functions of the wonderful package [scikit-allel](https://scikit-allel.readthedocs.io/en/stable/index.html) and it has been created from the desire of having a tool able to perform this conversion for downstram phylogenetic analyses. 

Especially for studies (uniparental researches) that include multi-VCF:

- is created not only from the merging of VCF self-produced from FASTQ, BAM files but also from the merging of VCFs given /  downloaded from public repository (for which is impossible obtain the raw data). 
- post-QC multi-VCF in which a manual curation of the SNPs has been performed and informative SNPs are included.

Other tools such as [bcftools](http://samtools.github.io/bcftools/bcftools.html#consensus) have the option to generate a consensus FASTA sequence starting from a VCF but they require a reference sequence and it makes the resulting FASTA much more longer than the set of informative SNPs that are required for a phylogenetic analysis. Selecting specific positions and or regions make the process cumbersome especially if all the information you want is only in the VCF you have just produced.

The script is commented and the workflow is in the notebook. Any suggestions, implementation are welcome!
