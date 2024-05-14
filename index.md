# Taxonomy Classifiers For Use With Q2-Feature-Classifier

```{image} ./static/images/qiime2-resources-ai-art.png
:alt: Qiime2 Resources AI Art
:align: left
```

:::{danger}
:header: **DANGER!**

Pre-trained classifiers that can be used with q2-feature-classifier currently present a security risk. If using a pre-trained classifier such as the ones provided here, you should trust the person who trained the classifier and the person who provided you with the qza file. This security risk will be addressed in a future version of q2-feature-classifier.
:::

:::{note}
:header: Note

Taxonomic classifiers perform best when they are trained based on your specific sample preparation and sequencing parameters, including the primers that were used for amplification and the length of your sequence reads. Therefore in general you should follow the instructions in [Training feature classifiers with q2-feature-classifier](https://docs.qiime2.org/2024.2/tutorials/feature-classifier/) to train your own taxonomic classifiers (for example, from the marker gene reference databases below).
:::

## QIIME 2 2021.4-2024.2:

### Naive Bayes Classifiers:

```{card}
:header: **Silva 138 99% OTUs full-length sequences**

**Download**: [Silva 138 99% OTUs full-length sequences](https://data.qiime2.org/2024.2/common/silva-138-99-nb-classifier.qza)\
**UUID**: 2bbe61fa-7f78-4913-a6a7-b42e6fff2279\
**SHA256**: bb5870fcf084e82a9ee6ca806f1b4f9e78b2e299eac608ff1dca4b2f28fb1b36\
**Sklearn-version**: 0.24.1\
**Notes**: [Silva species taxonomy may be unreliable](#Silva)\
**Citations**: @Robeson2020-ax, [Silva](#Silva-Citations)
```

```{card}
:header: **Silva 138 99% OTUs from 515F/806R region of sequences**

**Download**: [Silva 138 99% OTUs from 515F/806R region of sequences](https://data.qiime2.org/2024.2/common/silva-138-99-515-806-nb-classifier.qza)\
**UUID**: 9b9c290b-2297-4711-bafe-7cc603f3b990\
**SHA256**: 5b08f1c272b16208830b2b712a682824b82671c8b6c5fe325ccd7feabfc498ba\
**Sklearn-version**: 0.24.1\
**Notes**: [Silva species taxonomy may be unreliable](#Silva)\
**Citations**: @Robeson2020-ax, [Silva](#Silva-Citations)
```

```{card}
:header: **Greengenes2 2022.10 full length sequences**

**Download**: [Greengenes2 2022.10 full length sequences](https://data.qiime2.org/classifiers/greengenes/gg_2022_10_backbone_full_length.nb.qza)\
**UUID**: 3e819633-6888-42f9-ab66-fe5214e57d72\
**SHA256**: f48c1e2cc7b997d3dee953e1869c2492de03f31d99886f06a50b2536136ad5cf\
**Sklearn-version**: 0.24.1\
**Notes**: [Greengenes2 has succeeded Greengenes 13_8](#GG2)\
**Citations**: @McDonald2023-gq, @Bokulich2018-yb
```

```{card}
:header: **Greengenes2 2022.10 from 515F/806R region of sequences**

**Download**: [Greengenes2 2022.10 from 515F/806R region of sequences](https://data.qiime2.org/classifiers/greengenes/gg_2022_10_backbone.v4.nb.qza)\
**UUID**: 32489596-075f-44ff-a0ad-0a5c43a80b2c\
**SHA256**: 643fd395ada320140838f12c1d395fc88ae950128a83d3a3ac55625e1d21f337\
**Sklearn-version**: 0.24.1\
**Notes**: [Greengenes2 has succeeded Greengenes 13_8](#GG2)\
**Citations**: @McDonald2023-gq, @Bokulich2018-yb
```

### Weighted Taxonomic Classifiers:

These 16S rRNA gene classifiers were trained with weights that take into account the fact that not all species are equally likely to be observed. If your sample comes from any of the 14 habitat types we tested, these weighted classifiers should give you superior classification precision. If your sample doesn’t come from one of those habitats, they might still help. If you have the time, training with weights specific to your habitat should help even more. Weights for a range of habitats [are available here](https://github.com/BenKaehler/readytowear).


```{card}
:header: **Weighted Silva 138 99% OTUs full-length sequences**

**Download**: [Weighted Silva 138 99% OTUs full-length sequences](https://data.qiime2.org/2024.2/common/silva-138-99-nb-weighted-classifier.qza)\
**UUID**: 4df224fc-d4ba-44b6-9bef-cb0747673864\
**SHA256**: b0be3d168e7292f3f7d6d4a299e8a0f36416db013668e89f8e614e0bd648b452\
**Sklearn-version**: 0.24.1\
**Notes**: [Silva species taxonomy may be unreliable](#Silva)\
**Citations**: @Robeson2020-ax, @Kaehler2019-lq, [Silva](#Silva-Citations)
```

```{card}
:header: **Weighted Greengenes2 2022.10 full length sequences**

**Download**: [Weighted Greengenes 13_8 full length sequences](https://data.qiime2.org/2024.2/common/gg-13-8-99-nb-weighted-classifier.qza)\
**UUID**: 60645f71-cb57-41e3-8ed8-c3257a630cb7\
**SHA256**: 1629124485da77f5fadea213db4e5ba1361077df8b1fc1d37eafabc500251eca\
**Sklearn-version**: 0.24.1\
**Notes**: N/A\
**Citations**: @Kaehler2019-lq
```

```{card}
:header: **Greengenes2 2022.10 from 515F/806R region of sequences**

**Download**: [Weighted Greengenes 13_8 from 515F/806R region of sequences](https://data.qiime2.org/2024.2/common/gg-13-8-99-515-806-nb-weighted-classifier.qza)\
**UUID**: b607509d-cc1b-4fe7-863e-1359be7f34f3\
**SHA256**: eb4c11d7b3cf3d1d1f0ae40b47dcf2cd0c853f0b9f9e7594d257342ceb09103a\
**Sklearn-version**: 0.24.1\
**Notes**: N/A\
**Citations**: @Kaehler2019-lq
```

(Silva)=
:::{note}
:header: Note

The Silva classifiers provided here include species-level taxonomy. While Silva annotations do include species, Silva does not curate the species-level taxonomy so this information may be unreliable. In a future version of QIIME 2 we will no longer include species-level information in our Silva taxonomy classifiers. This is discussed on the QIIME 2 Forum [here](https://forum.qiime2.org/t/processing-filtering-and-evaluating-the-silva-database-and-other-reference-sequence-data-with-rescript/15494#heading--second-header) (see Species-labels: caveat emptor!).
:::

(GG2)=
:::{note}
:header: Note

Greengenes2 has succeeded Greengenes 13_8. If you still need to access the outdated 13_8 classifiers, for example to reproduce old results or to compare against new classifiers, you can access them through the older QIIME 2 data resources pages.
:::

(Silva-Citations)=
:::{note}
See the [SILVA website](https://www.arb-silva.de/) for the latest citation information for this reference database.
:::
