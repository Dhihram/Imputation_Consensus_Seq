# Treating Ambiguous Sequences with Consensus Sequence

We usually found the 'n' or 'N' as the ambiguous sequences in multiple alignment sequence. Ambiguous bases often arise due to sequencing errors, low coverage, or contamination, and they can impact downstream analyses like phylogenetics, 
SNP detection, and variant calling. If the ambiguous positions are due to sequencing errors or low coverage, replacing Ns with consensus-derived bases may be justified, provided the consensus is reliable. This method is an alternative when the reference
sequence is not available.

This method based on study:
* Sunguk Shin, Joonhong Park, Correction of sequence-dependent ambiguous bases (Ns) from the 454 pyrosequencing system, Nucleic Acids Research, Volume 42, Issue 7, 1 April 2014, Page e51, https://doi.org/10.1093/nar/gku070
* Gennady G Fedonin, Yury S Fantin, Alexnader V Favorov, German A Shipulin, Alexey D Neverov, VirGenA: a reference-based assembler for variable viral genomes, Briefings in Bioinformatics, Volume 20, Issue 1, January 2019, Pages 15–25, https://doi.org/10.1093/bib/bbx079

<p align="center">
  <img src="https://raw.githubusercontent.com/Dhihram/Imputation_Consensus_Seq/refs/heads/main/img/pre.png" alt="Pre processing.">
</p>


## Installing and using EMBOSS 

```{bash}
conda install bioconda::emboss
```
The consensus sequence is generated from multiple sequences.

```{bash}
cons -sequence sampel2.fasta -outseq consensus2.fasta
```

## Using code

The code can be check in the folder `code`

## Result

The ambiguous sequences are imputed by the consensus sequence

<p align="center">
  <img src="https://raw.githubusercontent.com/Dhihram/Imputation_Consensus_Seq/refs/heads/main/img/post.png" alt="Post processing.">
</p>

Alternatively, the ambiguous sequences are replaced by missing or '-'

<p align="center">
  <img src="https://raw.githubusercontent.com/Dhihram/Imputation_Consensus_Seq/refs/heads/main/img/post2.png">
</p>

