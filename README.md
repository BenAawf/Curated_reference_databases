# Curated_reference_databases

This repository contains the complete description of how we produced the curated reference databases for the studies in Evolutionary and Environmental Genomics Group ([@EvoHull](https://twitter.com/EVOHULL))


Currently, we have completed the curated reference databases of mitochondrial `12S `and `Cytb` including European freshwater fish, UK amphibians, UK birds, UK reptiles and UK mammals.

## Contents

#The contributors for each database as below:

__Cytb__

- [European freshwater fish](https://github.com/HullUni-bioinformatics/Curated_reference_databases/tree/master/Cytb_Fish) by Christoph Hahn `GitHub ID` [chrishah](https://github.com/chrishah)


__12S__
- [European freshwater fish](https://github.com/HullUni-bioinformatics/Curated_reference_databases/tree/master/12S_Fish) by Jianlong Li `GitHub ID` [JoeJianlongLi](https://github.com/JoeJianlongLi) and Christoph Hahn `GitHub ID` [chrishah](https://github.com/chrishah)

- [UK amphibians](https://github.com/HullUni-bioinformatics/Curated_reference_databases/tree/master/12S_Amphibians) by Lynsey R. Harper `GitHub ID` [lrharper1](https://github.com/lrharper1)

- [UK birds](https://github.com/HullUni-bioinformatics/Curated_reference_databases/tree/master/12S_Birds) by Lynsey R. Harper `GitHub ID` [lrharper1](https://github.com/lrharper1)

- [UK reptiles](https://github.com/HullUni-bioinformatics/Curated_reference_databases/tree/master/12S_Reptiles) by Lynsey R. Harper `GitHub ID` [lrharper1](https://github.com/lrharper1)

- [UK mammals](https://github.com/HullUni-bioinformatics/Curated_reference_databases/tree/master/12S_Mammals) by Lynsey R. Harper `GitHub ID` [lrharper1](https://github.com/lrharper1)


#Work your way through the notebooks in the individual directories in the following order with slightly changes between the databases:

- Convert_denovo_fasta_to_gb (If you do not have denovo fasta sequences, skip it)
- fetch-and-clean
- nr (We sometime combined `fetch-and-clean` and `nr` to `fetch_clean_align` or `fetch_clean_align_tree`)
- SATIVA
- post_SATIVA


__Final clean database__

You can find the final clean database which has been labeled by `*SATIVA_cleaned*.gb` ([for example](https://github.com/HullUni-bioinformatics/Curated_reference_databases/blob/master/12S_Amphibians/12S_UKamphibians_SATIVA_cleaned.gb)) in each database.


## Setting up the environment

To facilitate full reproducibility of our analyses we provide `Jupyter notebooks` illustrating our workflow in this repository.

In the individual directory listed above of each database, you can find the Jupyter notebooks `*.ipynb` ([for example](https://github.com/HullUni-bioinformatics/Curated_reference_databases/blob/master/12S_Amphibians/fetch_clean_align_tree/Amphib_align_clipping.ipynb)) which you can use them for reproducible analysis.

You need the [metaBEAT](https://github.com/HullUni-bioinformatics/metaBEAT) pipeline, which relies on a range of open bioinformatics tools, which we have wrapped up in a self contained docker image which includes all necessary dependencies [here](https://hub.docker.com/r/chrishah/metabeat/).

`metaBEAT` is using a number of external programs. To make your life easier we have created a self contained environment with all necessary pieces of software in a [docker image](https://hub.docker.com/r/chrishah/metabeat/). This image is building on [ReproPhylo](https://hub.docker.com/r/szitenberg/reprophylo/). If you want to use it you'll need Docker installed on your machine. 

The more details about how to install the `Docker` and `metaBEAT`, please go to visit the GitHub repository in [here](https://github.com/HullUni-bioinformatics/metaBEAT).

## Publications 
#The publications have used the curated reference databases in this repository

- Hänfling, B., Lawson Handley, L., Read, D.S.,  ... Winfield, I.J. (2016) Environmental DNA metabarcoding of lake fish communities reflects long-term data from established survey methods. _Molecular Ecology_, 25, 3101-3119. ([DOI](https://doi.org/10.1111/mec.13660)) ([GitHub](https://github.com/HullUni-bioinformatics/Haenfling_et_al_2016))  

- Harper, L.R., Lawson Handley, L., Hahn, C.,  ... Hänfling, B. (2018) Needle in a haystack? A comparison of eDNA metabarcoding and targeted qPCR for detection of the great crested newt (_Triturus cristatus_). _Ecology and Evolution_, 8, 6330-6341. ([DOI](https://doi.org/10.1002/ece3.4013)) ([GitHub](https://github.com/HullUni-bioinformatics/Harper_et_al_2018)) 

- Li, J., Lawson Handley, L.J., Read, D.S. & Hänfling, B. (2018) The effect of filtration method on the efficiency of environmental DNA capture and quantification via metabarcoding. _Molecular Ecology Resources_, 18, 1102-1114. ([DOI](https://doi.org/10.1111/1755-0998.12899)) ([GitHub](https://github.com/HullUni-bioinformatics/Li_et_al_2018_eDNA_filtration))  

- Sellers, G.S., Di Muri, C., Gomez, A. & Hänfling, B. (2018) Mu-DNA: a modular universal DNA extraction method adaptable for a wide range of sample types. _Metabarcoding and Metagenomics_, 2: e24556. ([DOI](https://mbmg.pensoft.net/articles.php?id=24556)) ([OSF](https://osf.io/vrb4a/)) 

- Li, J.,  Hatton‐Ellis, T.W., Lawson Handley, L.J.,... Hänfling, B. (2019) Ground‐truthing of a fish‐based environmental DNA metabarcoding method for assessing the quality of lakes. _Journal of Applied Ecology_, 56, 1232–1244. ([DOI](https://besjournals.onlinelibrary.wiley.com/doi/10.1111/1365-2664.13352)) ([GitHub](https://github.com/HullUni-bioinformatics/Li_et_al_2019_eDNA_fish_monitoring))

- Lawson Handley, L.J., Read, D.S., Winfield, I.J., ... Hänfling, B. (2019) Temporal and spatial variation in distribution of fish environmental DNA in England’s largest lake. _Environmental DNA_, 1, 26-39. ([DOI](https://onlinelibrary.wiley.com/doi/abs/10.1002/edn3.5)) ([GitHub](https://github.com/HullUni-bioinformatics/Handley_et_al_2019))

- Li, J., Lawson Handley, L.J., Harper, L.R.,... Hänfling, B. (2019) Limited dispersion and quick degradation of environmental DNA in fish ponds inferred by metabarcoding. _Environmental DNA_, 00, 1-13. ([DOI](https://onlinelibrary.wiley.com/doi/full/10.1002/edn3.24)) ([GitHub](https://github.com/HullUni-bioinformatics/Li_et_al_2019_eDNA_dynamic))
