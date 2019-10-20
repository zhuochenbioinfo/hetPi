# hetPi
Nucleotide diversity estimation using VCF input with special treatment for heterozygous genotypes

# Motivation:

In some plants, heterozygous genotypes can be stably present due to asexual reproduction (Such as grafting). Here I introduce a modified Pi estimate, hetPi, that treat heterozygous situation as an intermediate genotype. This estimate is based on [necleotide diversity π](https://doi.org/10.1073/pnas.76.10.5269) introduced by Nei and Li in 1979.

For a bi-allelic diploid SNP, the genetic distance of two samples carring two different homozygous genotype is set as 1. The distance between sample carring heterozygous genotype and sample carring any of the homozygous genotype is set as 0.5. The distance of two samples carring the same genotype, no matter homozygous or heterozygous, is zero.

# Usage:

The typical usage is:
`perl hetPi.pl --vcf in.vcf --out out.hetpi`

For additional variant filteration and window settings, please check the usage in the scripts or just run:

`perl hetPi.pl`

# Reference:

Wikipedia. https://en.wikipedia.org/wiki/Nucleotide_diversity
