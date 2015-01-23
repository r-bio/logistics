Heather Kates
R project


Research goal: 
Identify selective sweeps across the pumpkin exome based on multi-locus allele frequency differentiation between a modern improved crop, its wild ancestor, and its local landraces.

Project goal: 
Implement a recently published statistical analysis for detecting selective sweeps, XP-CLR (cross-population composite likelihood ratio) into an existing population genomics package for R, PopGenome. 

Data format:
~3,000 Multi-locus alignment files (.nexus) each with 90 individuals from three “populations”.

About PopGenome R package:
•	PopGenome’s modules are useful for many statistical tests (including CLR test for selective sweeps- CLR does not account for characteristic differences in allele frequencies across two populations that are expected to arise in the case of natural selection.) 
•	PopGenome specifically designed to simplify the integration of new methods. 
o	  function create.PopGenome.method(), which generates a skeleton of a typical PopGenome function.  
o	  New methods implemented are fully embedded in the PopGenome framework and can be applied to sliding window or sub-sites in the same way as PopGenome’s existing modules. 
•	Output data can be analyzed further using the built-in statistical and graphical capabilities of R., e.g. you can produce a figure that shows a plot of the sliding window nucleotide diversities with a simple R function.

Why implementing XP-CLR method in PopGenome?
•	Standard statistical tests used to test for signatures of selection and selective sweeps are available in the R package Popgenome.  However, the demographic processes shaping crop diversity may invalidates the assumptions of standard statistical tests for selection.  
o	  XP-CLR (Chen, 2010) is a cross population composite likelihood ratio test that can be likened to a measure of FST that looks at many loci and is robust to demographic history.  
•	The XP-CLR source code in C is limited to performing genome wide scans for selection via a sliding window, while the data in my project will be assembled into a multi-locus dataset.   The XP-CLR code also cannot account for missing data, which my dataset has.


Challenges: 
1) C and R:
•	The source code for XP-CLR is written in C.  
•	Most functions in PopGenome are implemented in C or C++.  
•	This project will require learning how to interface C code with R.  
o	  Ensure that the functions written in C have specific properties that allow them to be called by R. 
•	    1) They must return void, which means they need to return the results of the computation in their arguments.  
•	    2) All arguments passed to the C function are passed by reference, which means you pass a pointer to a number or array.  One must be careful to correctly dereference the pointers in the C code.  
•	    3) Each file containing C code to be called by R should include the R.h header. #include <R.h>  4) When compiling the C code, use R to do the compilation rather than the C compiler. This way R knows where all of the header files and libraries are located. (R CMD SHLIB XPCLR.c)

