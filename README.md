# omics-time-annotation
A supervised time annotation method for omics experiments using Gaussian processes 
    
## Motivation

Time course transcriptomics experiments have been widely used to explore essential biological processes that exhibit dynamic characteristics and generate hypothesis about them. However, time annotations could be missing, imprecise, or biologically inconsistent. Here we introduce a supervised method based on Gaussian Processes for assigning time annotation to omics experiments. 

## Installation and Dependencies

To run the method the following Python packages are required:
    
    GPy, pandas, numpy, scipy, matplotlib.pyplot

## Data format

To run the method we need a file with reference experiments and a file with the target experiments.

The reference experiments' file should have the following structure where experiments belonging to the same replicate are put next to each other and the time ordering is the same for each replicate:

    gene    t_1 Rep_1     t_2 Rep_1     t_3 Rep_1    ...    time_t Rep_1    t_1 Rep_2     t_2 Rep_2     t_3 Rep_2    ...    time_t Rep_2    .....    t_1 Rep_r     t_2 Rep_r     t_3 Rep_r    ...    time_t Rep_r
    gene_1  10            20            5            ...    8               10            20            5            ...    8               .....    10            20            5            ...    8
    gene_2  3             2             50           ...    8               10            20            5            ...    8               .....    10            20            5            ...    8
    gene_3  3             2             50           ...    8               10            20            5            ...    8               .....    10            20            5            ...    8
    ...
    gene_n  3             2             50           ...    8               10            20            5            ...    8               .....    10            20            5            ...    8


The target experiments' file should have the following structure:

    gene    Exp_1    Exp_2    ...    Exp_m    
    gene_1  10       20       ...    5            
    gene_2  3        2        ...    50         
    gene_3  3        2        ...    50          
    ...
    gene_n  3        2        ...    50        

## How to cite this material

DOI: 10.5281/zenodo.11075349
