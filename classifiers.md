# Taxonomy Classifiers For Use With Q2-feature-classifier

```{card}
:header: Note

Taxonomic classifiers perform best when they are trained based on your specific sample preparation and sequencing parameters, including the primers that were used for amplification and the length of your sequence reads. Therefore in general you should follow the instructions in [Training feature classifiers with q2-feature-classifier](https://docs.qiime2.org/2024.2/tutorials/feature-classifier/) to train your own taxonomic classifiers (for example, from the marker gene reference databases below).
```

```{list-table} Naive Bayes Classifiers
:header-rows: 1
:align: left

* - File URL
  - MD5 Sum
  - Artifact UUID
  - Notes
  - Citations
* - [Silva 138 99% OTUs full-length sequences](https://data.qiime2.org/2024.2/common/silva-138-99-nb-classifier.qza)
  - b8609f23e9b17bd4a1321a8971303310
  - placeholder
  - [Silva species taxonomy may be unreliable](#Silva)
  - [1](#Silva-Citations)
* - [Silva 138 99% OTUs from 515F/806R region of sequences](https://data.qiime2.org/2024.2/common/silva-138-99-515-806-nb-classifier.qza)
  - e05afad0fe87542704be96ff483824d4
  - placeholder
  - [Silva species taxonomy may be unreliable](#Silva)
  - [1](#Silva-Citations)
* - [Greengenes2 2022.10 full length sequences](https://data.qiime2.org/classifiers/greengenes/gg_2022_10_backbone_full_length.nb.qza)
  - 98d34227fe67b34f62b464466cca4ffa
  - placeholder
  - [Greengenes2 has succeeded Greengenes 13_8](#GG2)
  - [2](#GG2-Citations),[3](#GG2-NB-Citations)
* - [Greengenes2 2022.10 from 515F/806R region of sequences](https://data.qiime2.org/classifiers/greengenes/gg_2022_10_backbone.v4.nb.qza)
  - 43de361005ae6dcae61b078c0c835021
  - placeholder
  - [Greengenes2 has succeeded Greengenes 13_8](#GG2)
  - [2](GG2-Citations),[3](#GG2-NB-Citations)
```

(Silva)=
```{card}
:header: Note

The Silva classifiers provided here include species-level taxonomy. While Silva annotations do include species, Silva does not curate the species-level taxonomy so this information may be unreliable. In a future version of QIIME 2 we will no longer include species-level information in our Silva taxonomy classifiers. This is discussed on the QIIME 2 Forum [here](https://forum.qiime2.org/t/processing-filtering-and-evaluating-the-silva-database-and-other-reference-sequence-data-with-rescript/15494#heading--second-header) (see Species-labels: caveat emptor!).
```


(GG2)=
```{card}
:header: Note

Greengenes2 has succeeded Greengenes 13_8. If you still need to access the outdated 13_8 classifiers, for example to reproduce old results or to compare against new classifiers, you can access them through the older QIIME 2 data resources pages.
```

## Weighted Taxonomic Classifiers

These 16S rRNA gene classifiers were trained with weights that take into account the fact that not all species are equally likely to be observed. If your sample comes from any of the 14 habitat types we tested, these weighted classifiers should give you superior classification precision. If your sample doesn’t come from one of those habitats, they might still help. If you have the time, training with weights specific to your habitat should help even more. Weights for a range of habitats [are available here](https://github.com/BenKaehler/readytowear).

```{list-table} Weigthed Classifiers
:header-rows: 1
:align: left

* - File URL
  - MD5 Sum
  - Artifact UUID
  - Notes
  - Citations
* - [Weighted Silva 138 99% OTUs full-length sequences](https://data.qiime2.org/2024.2/common/silva-138-99-nb-weighted-classifier.qza)
  - 48965bb0a9e63c411452a460d92cfc04
  - placeholder
  - [Silva species taxonomy may be unreliable](#Silva)
  - [1](#Silva-Citations),[4](#Weighted-Citations)
* - [Weighted Greengenes 13_8 full length sequences](https://data.qiime2.org/2024.2/common/gg-13-8-99-nb-weighted-classifier.qza)
  - 2baf87fce174c5f6c22a4c4086b1f1fe
  - placeholder
  - N/A
  - [2](#GG2-Citations),[4](#Weighted-Citations)
* - [Weighted Greengenes 13_8 from 515F/806R region of sequences](https://data.qiime2.org/2024.2/common/gg-13-8-99-515-806-nb-weighted-classifier.qza)
  - 8fb808c4af1c7526a2bdfaafa764e21f
  - placeholder
  - N/A
  - [2](GG2-Citations),[4](#Weighted-Citations)
```

(Silva-Citations)=
For Silva 138, please cite the following references if you use any of these pre-trained classifiers:

    Michael S Robeson II, Devon R O’Rourke, Benjamin D Kaehler, Michal Ziemski, Matthew R Dillon, Jeffrey T Foster, Nicholas A Bokulich. RESCRIPt: Reproducible sequence taxonomy reference database management for the masses. bioRxiv 2020.10.05.326504; doi: https://doi.org/10.1101/2020.10.05.326504

    Bokulich, N.A., Kaehler, B.D., Rideout, J.R. et al. Optimizing taxonomic classification of marker-gene amplicon sequences with QIIME 2’s q2-feature-classifier plugin. Microbiome 6, 90 (2018). https://doi.org/10.1101/2020.10.05.326504

See the SILVA website for the latest citation information for this reference database.

(GG2-Citations)=
For Greengenes2, please cite:

    McDonald, D. et al. Greengenes2 unifies microbial data in a single reference tree. Nature Biotechnology (2023). https://www.nature.com/articles/s41587-023-01845-1

(GG2-NB-Citations)=
If using the Naive Bayes classifiers with Greengenes2, please cite:

    Bokulich, N.A., Kaehler, B.D., Rideout, J.R. et al. Optimizing taxonomic classification of marker-gene amplicon sequences with QIIME 2’s q2-feature-classifier plugin. Microbiome 6, 90 (2018). https://doi.org/10.1186/s40168-018-0470-z

(Weighted-Citations)=
Please cite the following reference, in addition to those listed above, if you use any of these weighted pre-trained classifiers:

    Kaehler, B.D., Bokulich, N.A., McDonald, D. et al. Species abundance information improves sequence taxonomy classification accuracy. Nature Communications 10, 4643 (2019). https://doi.org/10.1038/s41467-019-12669-6


