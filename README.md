# Investigating the Protective Role of the Mitochondrial 2158 T > C Variant in Parkinson’s Disease

`GP2 ❤️ Open Science 😍`

*DOI PENDING*

**Last Updated:** April 2024 

## Summary
This is the online repository for the short report titled ***"Investigating the Protective Role of the Mitochondrial 2158 T > C Variant in Parkinson’s Disease"***. This study aims to question the protective effect of a rare variant against Parkinson's disease in GP2, AllofUs, AMP-PD, and GenomicsEngland.

### Data Statement 
* All GP2 data are hosted in collaboration with the Accelerating Medicines Partnership in Parkinson's Disease and are available via application on the website. The GP2 PD case and control data are available via the GP2 website (https://gp2.org; release 6: https://doi.org/10.5281/zenodo.10472143). Genotyping imputation, quality control, ancestry prediction, and processing were performed using GenoTools (v1.0.0), publicly available on GitHub
* The All of Us genomic data are available under restricted access for human subject data. Access can be obtained by following the instructions under the All of Us workbench
* Primary data from the 100KGP, which are held in a secure Research Environment, are available to registered users. Please see https://www.genomicsengland.co.uk/about-gecip/for-gecip-members/data-and-data-access for further information

### Helpful Links 
- [GP2 Website](https://gp2.org/)
    - [GP2 Cohort Dashboard](https://gp2.org/cohort-dashboard-advanced/)
- [Introduction to GP2](https://movementdisorders.onlinelibrary.wiley.com/doi/10.1002/mds.28494)
    - [Other GP2 Manuscripts (PubMed)](https://pubmed.ncbi.nlm.nih.gov/?term=%22global+parkinson%27s+genetics+program%22)


# Repository Orientation 
- The `analyses/` directory includes all analyses discussed in the manuscript
    - `GP2/` includes 2 notebooks on processing and analyzing GP2 monogenic data from release 6

```
THIS_REPO
├── README.md
└── analyses
    ├── AMP-PD
    │   └── 00_AMPPD_Data_Prep.ipynb
    ├── AllOfUs
    │   ├── 00_AoU_Prep_Analysis_Controlsover70.ipynb
    │   ├── 01_AoU_Prep_Analysis_Cases.ipynb
    │   └── 02_AoU_Prep_Analysis_MaternalProxies.ipynb
    └── GP2
        ├── 00_GP2_Data_Prep.ipynb
        └── 01_GP2_Analysis.ipynb
```

---
### Analysis Notebooks
* Languages: Python, bash, and R

| **Directory** | Notebooks        | Description                        |
|---------------|------------------|------------------------------------|
| GP2/          | 00_GP2_Data_Prep | Downloading and structuring data   |
|               | 01_GP2_Analysis  | Running regression adjusted by PCs |
| AllOfUs/          | 00_AoU_Prep_Analysis_Controlsover70 | Querying and processing crams for neurologically healthy controls >70 + analysis  |
|           | 01_AoU_Prep_Analysis_Cases | Querying and processing crams for PD cases + analysis   |
|           | 02_AoU_Prep_Analysis_MaternalProxies | Querying and processing crams for maternal proxy PD cases + analysis  |
| AMP-PD/          | 00_AMPPD_Data_Prep | Downloading and structuring data from AMP-PD  |

---

# Software 
|               Software              |  Version(s) |                              Resource URL                              |       RRID      |                                               Notes                                               |   |
|:-----------------------------------:|:-----------:|:----------------------------------------------------------------------:|:---------------:|:-------------------------------------------------------------------------------------------------:|:-:|
|     Python Programming Language     | 3.8 and 3.9 |                         http://www.python.org/                         | RRID:SCR_008394 | pandas; numpy; seaborn; matplotlib; statsmodel; used for general data wrangling/plotting/analyses |   |
| R Project for Statistical Computing |     4.2     |                        http://www.r-project.org/                       | RRID:SCR_001905 |   tidyverse; dplyr; tidyr; ggplot; data.table; used for general data wrangling/plotting/analyses  |   |
|                PLINK                |     2.0     |                   http://www.nitrc.org/projects/plink                  | RRID:SCR_001757 |                                     used for genetic analyses                                     |   |
|         samtools (bcftools)         |     1.9     |                         https://www.htslib.org/                        | RRID:SCR_002105 |                                          VCF manipulation                                         |   |
|            GATK (Mutect2)           |    4.5.0    | https://gatk.broadinstitute.org/hc/en-us/articles/360037593851-Mutect2 | RRID:SCR_001876 |                   call somatic SNVs and indels via local assembly of haplotypes                   |   |
