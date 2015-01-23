R project notes

Part 1: Analyze differences in mRNA expression patterns between two types of embyronic tissue (anterior vs. posterior oral palate from a mouse embryo). I have these data in Galaxy and I intend to process them through a specific pipeline that includes the R package CummeRbund. I have 50 bp single-end reads from Illumina Hi-Seq, 3 replicates per sample. 
These data sets will require significant processing before running CummeRbund (Fastq groomer clean-up, Bowtie, TopHat, Cufflinks, Cuffdiff, then finally CummeRbund.) I'm also interested in learning how to manipulate large text files in R.

R packages:  CummeRbund, and others?

Part 2: Statistical analysis of morphometric data from fossil and extant mammals. I have both continuous and discrete morphological data, so I am interested in trying packages that specialize with either (or both) kinds of data. The goal of these analyses is to test whether particular morphological variables are correlated with each other, and also to investigate how these variables scale with body size (allometrically or isometrically) in different taxa (predominantly rodents).

R Packages: lmodel2 (Major Axis regression), and others ??. I gave the lmodel2 package a try this week and it seems to work!

Part 3: Comparative phylogenetics: Ancestral state reconstruction, mapping other data on trees. This is essentially a continuation of Part 2 using the same morphological data to examine macroevolutionary patterns within mammals. (I was initially planning to use Mesquite, but if I can use R for this, I'd be much happier!) I plan to map data onto a mammal supertree and onto smaller tree(s) as well. The supertree should be completed within 2 weeks and the smaller trees I've already re-analyzed from others' previously published work.  

R packages for phylogenetic comparative methods: ape, geiger, caper, phytools, maybe phylobase?
