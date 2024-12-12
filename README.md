# Treating Ambiguous Sequences with Consensus Sequence

We usually found the 'n' or 'N' as the ambiguous sequences in multiple alignment sequence. Ambiguous bases often arise due to sequencing errors, low coverage, or contamination, and they can impact downstream analyses like phylogenetics, 
SNP detection, and variant calling. If the ambiguous positions are due to sequencing errors or low coverage, replacing Ns with consensus-derived bases may be justified, provided the consensus is reliable. This method is an alternative when the `.vcf` 
file is not available.


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

