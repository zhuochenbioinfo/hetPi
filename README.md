# hetPi
Nucleotide diversity estimation using VCF input with special treatment for heterozygous genotypes

By Zhuo CHEN, contact: chenomics@163.com or zhuochen@fafu.edu.cn

# Motivation:

In some plants, heterozygous genotypes can be stably present due to asexual reproduction (such as grafting). Here I introduce a modified Pi estimate, hetPi, that treat heterozygous situation as an intermediate genotype. This estimate is based on [necleotide diversity π](https://doi.org/10.1073/pnas.76.10.5269) introduced by Nei and Li in 1979.

For a bi-allelic diploid SNP, the genetic distance between two samples carrying two different homozygous genotypes is set as 1. The distance between a sample carrying heterozygous genotype and a sample carrying any of the homozygous genotypes is set as 0.5. The distance of two samples carrying the same genotype, no matter homozygous or heterozygous, is zero.

# Usage:

This program treat bi-allelic, diploid SNPs only.

The typical usage is:

`perl hetPi.pl --vcf in.vcf --out out.hetpi`

For additional sample or variant filteration and window settings, please check the usage in the scripts or just run:

`perl hetPi.pl`

# Reference:

Nei, M. and W. H. Li (1979). "Mathematical model for studying genetic variation in terms of restriction endonucleases." Proc. Natl. Acad. Sci. U. S. A. 76(10): 5269-5273.

Wikipedia. https://en.wikipedia.org/wiki/Nucleotide_diversity
