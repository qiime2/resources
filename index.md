(taxonomic-classifiers)=
# Taxonomic classifiers

This page provides pre-trained taxonomic classifiers that can be used with the `q2-feature-classifier` plugin (@Bokulich2018-yb).
Classifiers are specific to versions of [scikit-learn](https://scikit-learn.org/) (@scikit-learn), a dependency of `q2-feature-classifier`, and thus are categorized below by the QIIME 2 version range that they will work with.

:::{danger} Security risk


**Pre-trained classifiers that can be used with q2-feature-classifier currently present a security risk.**
This is due to the fact that unlike most QIIME 2 artifacts that only contain data, **classifiers contain [serialized Python objects](https://scikit-learn.org/stable/model_persistence.html) that contain a program that will run on your computer**.
We have no way of vetting these programs and making sure they are safe.

If using a pre-trained classifier, such as the ones provided here, you should trust the person who trained the classifier and the person who provided you with it.

After downloading a classifier from this page, it is a very good idea to calculate the [sha256 sum](https://www.movable-type.co.uk/scripts/sha256.html) of the classifier using the command `shasum -a 256 <path-to-classifier>`.
If the output does not match the `SHA256` value associated with the classifier on this page, do not use the classifier and instead re-download it from this page.
If this persists after you try downloading multiple times, please let us know on the [QIIME 2 Forum](https://forum.qiime2.org).

The safest thing to do, if you're concerned about using these classifiers, is to [train your own classifiers with QIIME 2](https://docs.qiime2.org/2024.2/tutorials/feature-classifier/) rather than download existing ones.

We hope to [address this security risk](https://github.com/qiime2/q2-feature-classifier/issues/202) in a future version of q2-feature-classifier.
If you have relevant expertise and would like to help with this, we would welcome that!
:::

:::{note}
:header: Note

Taxonomic classifiers perform best when they are trained based on your specific sample preparation and sequencing parameters, including the primers that were used for amplification and the length of your sequence reads. Therefore in general you should follow the instructions in [Training feature classifiers with q2-feature-classifier](https://docs.qiime2.org/2024.2/tutorials/feature-classifier/) to train your own taxonomic classifiers (for example, from the marker gene reference databases below).
:::

## QIIME 2 2024.5 - Present

### Naive Bayes Classifiers

```{card}
:header: **Silva 138 99% OTUs full-length sequences**

**Download**: [Silva 138 99% OTUs full-length sequences](https://data.qiime2.org/classifiers/sklearn-1.4.2/silva/silva-138-99-nb-classifier.qza)\
**UUID**: 70b4b5f4-8fce-40bd-b508-afacbc12a5ed\
**SHA256**: c08a1aa4d56b449b511f7215543a43249ae9c54b57491428a7e5548a62613616\
**Sklearn Version**: 1.4.2\
**Date Trained**: 2024-05-30\
**Notes**: [Silva species taxonomy may be unreliable](#Silva)\
**Citations**: @Robeson2020-ax, @Bokulich2018-yb, [Silva](#Silva-Citations)
```

```{card}
:header: **EXPERIMENTAL: diverse weighted Silva 138 99% OTUs full-length sequences**

**Download**: [diverse weighted Silva 138 99% OTUs full-length sequences](https://data.qiime2.org/classifiers/sklearn-1.4.2/silva/silva-138-99-nb-diverse-weighted-classifier.qza)\
**UUID**: eff4efb9-d90d-43ce-acb3-53e04583323a\
**SHA256**: decfae408061fab8ff2fec7dac1fe2a2e0041581589715062cc789bd4f9933db\
**Sklearn Version**: 1.4.2\
**Date Trained**: 2024-07-04\
**Notes**: [Silva species taxonomy may be unreliable. These classifiers were created with 14 diverse environments: "Sediment (non-saline)", "Plant corpus", "Animal secretion", "Sediment (saline)", "Animal surface", "Surface (saline)",  "Plant rhizosphere",  "Soil (non-saline)", "Animal distal gut", "Water (saline)",  "Animal proximal gut", "Water (non-saline)",  "Animal corpus", "Plant surface". More information can be found at: https://www.nature.com/articles/s41467-019-12669-6](#Silva)\
**Citations**: @Robeson2020-ax, @Bokulich2018-yb, @Kaehler2019-lq, [Silva](#Silva-Citations)
```

```{card}
:header: **EXPERIMENTAL: human stool weighted Silva 138 99% OTUs full-length sequences**

**Download**: [experimental human stool weighted Silva 138 99% OTUs full-length sequences](https://data.qiime2.org/classifiers/sklearn-1.4.2/silva/silva-138-99-nb-human-stool-weighted-classifier.qza)\
**UUID**: 529fdee1-778e-4a1e-acd2-b1b78fcc0048\
**SHA256**: db9e3c0105b1b9173deaa8bd828113b422c467443587cc8be3aed2e6f7cc995f\
**Sklearn Version**: 1.4.2\
**Date Trained**: 2024-05-30\
**Notes**: [Silva species taxonomy may be unreliable](#Silva)\
**Citations**: @Robeson2020-ax, @Bokulich2018-yb, @Kaehler2019-lq [Silva](#Silva-Citations)
```

```{card}
:header: **GTDB r220 full-length sequences**

**Download**: [GTDB r220 full-length sequences](https://data.qiime2.org/classifiers/sklearn-1.4.2/gtdb/gtdb_classifier_r220.qza)\
**UUID**: 5d5461cc-6a51-434b-90ab-040f388e4221\
**SHA256**: 07aadcf7472d9cc6f853f6b4615348619f1a3eceb56c1fb1b6d8dbb20554765f\
**Sklearn Version**: 1.4.2\
**Date Trained**: 2024-05-30\
**Citations**: @Parks2021, @Parks2020, @Parks2018, @Rinke2021
```

```{card}
:header: **EXPERIMENTAL: diverse weighted GTDB r220 full-length sequences**

**Download**: [diverse weighted GTDB r220 full-length sequences](https://data.qiime2.org/classifiers/sklearn-1.4.2/gtdb/gtdb_diverse_weighted_classifier_r220.qza)\
**UUID**: 5381b6fc-9f93-4844-8104-5263d5eae3f0\
**SHA256**: 232e0360f5e12f5158f2891db8d50de7e9cc035e1ea13672d9f87582ce10ee0f\
**Sklearn Version**: 1.4.2\
**Date Trained**: 2024-07-09\
**Notes**: [These classifiers were created with 14 diverse environments: "Sediment (non-saline)", "Plant corpus", "Animal secretion", "Sediment (saline)", "Animal surface", "Surface (saline)",  "Plant rhizosphere",  "Soil (non-saline)", "Animal distal gut", "Water (saline)",  "Animal proximal gut", "Water (non-saline)",  "Animal corpus", "Plant surface". More information can be found at: https://www.nature.com/articles/s41467-019-12669-6 ](#GTDB)\
**Citations**: @Parks2021, @Parks2020, @Parks2018, @Rinke2021, @Kaehler2019-lq
```

```{card}
:header: **EXPERIMENTAL: human stool weighted GTDB r220 full-length sequences**

**Download**: [experimental human stool weighted GTDB r220 full-length sequences](https://data.qiime2.org/classifiers/sklearn-1.4.2/gtdb/gtdb_human_stool_weighted_classifier_r220.qza)\
**UUID**: 4410ca00-2484-49ef-bad5-039e82be10b9\
**SHA256**: ec15dec8adc9f0bd45b315117df968a551651aef495a6079541a8bb29225d522\
**Sklearn Version**: 1.4.2\
**Date Trained**: 2024-05-30\
**Notes**: [GTDB human stool weights provide unreliable results for Bacteriodes taxa](#GTDB)
**Citations**: @Parks2021, @Parks2020, @Parks2018, @Rinke2021, @Kaehler2019-lq
```

```{card}
:header: **Greengenes2 2022.10 full length sequences**

**Download**: [Greengenes2 2022.10 full length sequences](https://data.qiime2.org/classifiers/sklearn-1.4.2/greengenes2/2022.10.backbone.full-length.nb.sklearn-1.4.2.qza)\
**UUID**: 1df1eab1-2ee4-4d92-917e-ba1f6c937269\
**SHA256**: 4f7ab05b57f85a76b12049c057c363759112fe17b7337f69f1ab2db0ec668024\
**Sklearn Version**: 1.4.2\
**Date Trained**: 2024-05-15\
**Forum Submitter**: [wasade](https://forum.qiime2.org/u/wasade/summary)\
**Notes**: [Greengenes2 has succeeded Greengenes 13_8](#GG2)\
**Citations**: @McDonald2023-gq, @Bokulich2018-yb
```

```{card}
:header: **Greengenes2 2022.10 from 515F/806R region of sequences**

**Download**: [Greengenes2 2022.10 from 515F/806R region of sequences](https://data.qiime2.org/classifiers/sklearn-1.4.2/greengenes2/2022.10.backbone.v4.nb.sklearn-1.4.2.qza)\
**UUID**: c0a78f62-6d0f-4f4a-b9c1-ec34c4b4763b\
**SHA256**: 5784f50a4ce8f004019ae7495e83c170aecdb4126aa13f0bb1b2e78d1f5cb024\
**Sklearn Version**: 1.4.2\
**Date Trained**: 2024-05-15\
**Forum Submitter**: [wasade](https://forum.qiime2.org/u/wasade/summary)\
**Notes**: [Greengenes2 has succeeded Greengenes 13_8](#GG2)\
**Citations**: @McDonald2023-gq, @Bokulich2018-yb
```

## QIIME 2 2021.4-2024.2

### Naive Bayes Classifiers

```{card}
:header: **Silva 138 99% OTUs full-length sequences**

**Download**: [Silva 138 99% OTUs full-length sequences](https://data.qiime2.org/2024.2/common/silva-138-99-nb-classifier.qza)\
**UUID**: 2bbe61fa-7f78-4913-a6a7-b42e6fff2279\
**SHA256**: bb5870fcf084e82a9ee6ca806f1b4f9e78b2e299eac608ff1dca4b2f28fb1b36\
**Sklearn Version**: 0.24.1\
**Date Trained**: 2021-05-09\
**Notes**: [Silva species taxonomy may be unreliable](#Silva)\
**Citations**: @Robeson2020-ax, @Bokulich2018-yb, [Silva](#Silva-Citations)
```

```{card}
:header: **Silva 138 99% OTUs from 515F/806R region of sequences**

**Download**: [Silva 138 99% OTUs from 515F/806R region of sequences](https://data.qiime2.org/2024.2/common/silva-138-99-515-806-nb-classifier.qza)\
**UUID**: 9b9c290b-2297-4711-bafe-7cc603f3b990\
**SHA256**: 5b08f1c272b16208830b2b712a682824b82671c8b6c5fe325ccd7feabfc498ba\
**Sklearn Version**: 0.24.1\
**Date Trained**: 2021-05-07\
**Notes**: [Silva species taxonomy may be unreliable](#Silva)\
**Citations**: @Robeson2020-ax, @Bokulich2018-yb, [Silva](#Silva-Citations)
```

```{card}
:header: **Greengenes2 2022.10 full length sequences**

**Download**: [Greengenes2 2022.10 full length sequences](https://data.qiime2.org/classifiers/greengenes/gg_2022_10_backbone_full_length.nb.qza)\
**UUID**: 3e819633-6888-42f9-ab66-fe5214e57d72\
**SHA256**: f48c1e2cc7b997d3dee953e1869c2492de03f31d99886f06a50b2536136ad5cf\
**Sklearn Version**: 0.24.1\
**Date Trained**: 2022-12-30\
**Forum Submitter**: [wasade](https://forum.qiime2.org/u/wasade/summary)\
**Notes**: [Greengenes2 has succeeded Greengenes 13_8](#GG2)\
**Citations**: @McDonald2023-gq, @Bokulich2018-yb
```

```{card}
:header: **Greengenes2 2022.10 from 515F/806R region of sequences**

**Download**: [Greengenes2 2022.10 from 515F/806R region of sequences](https://data.qiime2.org/classifiers/greengenes/gg_2022_10_backbone.v4.nb.qza)\
**UUID**: 32489596-075f-44ff-a0ad-0a5c43a80b2c\
**SHA256**: 643fd395ada320140838f12c1d395fc88ae950128a83d3a3ac55625e1d21f337\
**Sklearn Version**: 0.24.1\
**Date Trained**: 2022-10-20\
**Forum Submitter**: [wasade](https://forum.qiime2.org/u/wasade/summary)\
**Notes**: [Greengenes2 has succeeded Greengenes 13_8](#GG2)\
**Citations**: @McDonald2023-gq, @Bokulich2018-yb
```

```{card}
:header: **Greengenes 13_8 99% OTUs full length sequences**

**Download**: [Greengenes 13_8 99% OTUs full length sequences](https://data.qiime2.org/2022.11/common/gg-13-8-99-nb-classifier.qza)\
**UUID**: aacdcb16-5bad-48f7-ac7d-3f30c35b0d67\
**SHA256**: b49f6e28e4b3195b39efb4787cd3c07d4c7a2fd5ba07f5699f95c3120de7a6b5\
**Sklearn Version**: 0.24.1\
**Date Trained**: 2021-04-21\
**Notes**: N/A\
**Citations**: @Robeson2020-ax, @Bokulich2018-yb
```

```{card}
:header: **Greengenes 13_8 99% OTUs from 515F/806R region of sequences**

**Download**: [Greengenes 13_8 99% OTUs from 515F/806R region of sequences](https://data.qiime2.org/2022.11/common/gg-13-8-99-515-806-nb-classifier.qza)\
**UUID**: 4b2a57b7-1e5a-4a4d-8201-99551ab50858\
**SHA256**: 526a122e7599f542f6b76840097c3e5dbf71a13aed7e06fee595efce43578544\
**Sklearn Version**: 0.24.1\
**Date Trained**: 2021-04-21\
**Notes**: N/A\
**Citations**: @Robeson2020-ax, @Bokulich2018-yb
```

### Weighted Taxonomic Classifiers

These 16S rRNA gene classifiers were trained with weights that take into account the fact that not all species are equally likely to be observed.
If your sample comes from any of the 14 habitat types we tested, these weighted classifiers should give you superior classification precision.
If your sample doesn’t come from one of those habitats, they might still help.
If you have the time, training with weights specific to your habitat should help even more.
Weights for a range of habitats [are available here](https://github.com/BenKaehler/readytowear).


```{card}
:header: **Weighted Silva 138 99% OTUs full-length sequences**

**Download**: [Weighted Silva 138 99% OTUs full-length sequences](https://data.qiime2.org/2024.2/common/silva-138-99-nb-weighted-classifier.qza)\
**UUID**: 4df224fc-d4ba-44b6-9bef-cb0747673864\
**SHA256**: b0be3d168e7292f3f7d6d4a299e8a0f36416db013668e89f8e614e0bd648b452\
**Sklearn Version**: 0.24.1\
**Date Trained**: 2021-05-06\
**Notes**: [Silva species taxonomy may be unreliable](#Silva)\
**Citations**: @Robeson2020-ax, @Kaehler2019-lq, @Bokulich2018-yb, [Silva](#Silva-Citations)
```

```{card}
:header: **Weighted Greengenes 13_8 full length sequences**

**Download**: [Weighted Greengenes 13_8 full length sequences](https://data.qiime2.org/2024.2/common/gg-13-8-99-nb-weighted-classifier.qza)\
**UUID**: 60645f71-cb57-41e3-8ed8-c3257a630cb7\
**SHA256**: 1629124485da77f5fadea213db4e5ba1361077df8b1fc1d37eafabc500251eca\
**Sklearn Version**: 0.24.1\
**Date Trained**: 2021-04-21\
**Notes**: N/A\
**Citations**: @Kaehler2019-lq, @Bokulich2018-yb
```

```{card}
:header: **Weighted Greengenes 13_8 from 515F/806R region of sequences**

**Download**: [Weighted Greengenes 13_8 from 515F/806R region of sequences](https://data.qiime2.org/2024.2/common/gg-13-8-99-515-806-nb-weighted-classifier.qza)\
**UUID**: b607509d-cc1b-4fe7-863e-1359be7f34f3\
**SHA256**: eb4c11d7b3cf3d1d1f0ae40b47dcf2cd0c853f0b9f9e7594d257342ceb09103a\
**Sklearn Version**: 0.24.1\
**Date Trained**: 2021-04-21\
**Notes**: N/A\
**Citations**: @Kaehler2019-lq, @Bokulich2018-yb
```

## QIIME 2 2020.6-2021.2

### Naive Bayes Classifiers

```{card}
:header: **Silva 138 99% OTUs full-length sequences**

**Download**: [Silva 138 99% OTUs full-length sequences](https://data.qiime2.org/2021.2/common/silva-138-99-nb-classifier.qza)\
**UUID**: 50d540a8-272f-4012-86d3-31254047b46b\
**SHA256**: def48c9f9c8c3444f42b13dbeaf5f6376efff3e8e81994788dc3493fe02aaedc\
**Sklearn Version**: 0.23.1\
**Date Trained**: 2020-06-18\
**Notes**: [Silva species taxonomy may be unreliable](#Silva)\
**Citations**: @Robeson2020-ax, @Bokulich2018-yb, [Silva](#Silva-Citations)
```

```{card}
:header: **Silva 138 99% OTUs from 515F/806R region of sequences**

**Download**: [Silva 138 99% OTUs from 515F/806R region of sequences](https://data.qiime2.org/2021.2/common/silva-138-99-515-806-nb-classifier.qza)\
**UUID**: 981abf7d-2d85-41f5-963f-06e36c6ae5c5\
**SHA256**: 850d449c7b0b6833cf7d7d631fb4a462e72b21fbd41ac6e6b07f159c07f64c16\
**Sklearn Version**: 0.23.1\
**Date Trained**: 2020-06-17\
**Notes**: [Silva species taxonomy may be unreliable](#Silva)\
**Citations**: @Robeson2020-ax, @Bokulich2018-yb, [Silva](#Silva-Citations)
```

```{card}
:header: **Greengenes 13_8 99% OTUs full-length sequences**

**Download**: [Greengenes 13_8 99% OTUs full-length sequences](https://data.qiime2.org/2021.2/common/gg-13-8-99-nb-classifier.qza)\
**UUID**: 8390eae6-498b-410d-a042-4a997ceab50d\
**SHA256**: bf3604186bd7bde518bbe78478db3dd28b5ce383ae969d0efd7f8acdbd619734\
**Sklearn Version**: 0.23.1\
**Date Trained**: 2020-06-17\
**Notes**: N/A\
**Citations**: @McDonald2023-gq, @Bokulich2018-yb
```

```{card}
:header: **Greengenes 13_8 99% OTUs from 515F/806R region of sequences**

**Download**: [Greengenes 13_8 99% OTUs from 515F/806R region of sequences](https://data.qiime2.org/2021.2/common/gg-13-8-99-515-806-nb-classifier.qza)\
**UUID**: 0ad07fee-e9e8-48fa-8e35-9f689e324245\
**SHA256**: 2dd6f94a3614d5a1b8de6b6b1661a1e1bbb8778e53cbfcc47eb32989b5582895\
**Sklearn Version**: 0.23.1\
**Date Trained**: 2020-06-17\
**Notes**: N/A\
**Citations**: @McDonald2023-gq, @Bokulich2018-yb
```

## QIIME 2 2020.2

### Naive Bayes Classifiers

```{card}
:header: **Silva 132 99% OTUs full-length sequences**

**Download**: [Silva 132 99% OTUs full-length sequences](https://data.qiime2.org/2020.2/common/silva-132-99-nb-classifier.qza)\
**UUID**: 50d540a8-272f-4012-86d3-31254047b46b\
**SHA256**: 6a78f2a6a026c4a7b7b69f87ddec765d8ff6d933fc7681badeaac9338c439658\
**Sklearn Version**: 0.22.1\
**Date Trained**: 2020-02-18\
**Notes**: [Silva species taxonomy may be unreliable](#Silva)\
**Citations**: @Robeson2020-ax, @Bokulich2018-yb, [Silva](#Silva-Citations)
```

```{card}
:header: **Silva 132 99% OTUs from 515F/806R region of sequences**

**Download**: [Silva 132 99% OTUs from 515F/806R region of sequences](https://data.qiime2.org/2020.2/common/silva-132-99-515-806-nb-classifier.qza)\
**UUID**: 981abf7d-2d85-41f5-963f-06e36c6ae5c5\
**SHA256**: c541fe3087f2b1a2391082ab608256f6467022e04e54d3c07e28c1d51cb51f75\
**Sklearn Version**: 0.22.1\
**Date Trained**: 2020-02-18\
**Notes**: [Silva species taxonomy may be unreliable](#Silva)\
**Citations**: @Robeson2020-ax, @Bokulich2018-yb, [Silva](#Silva-Citations)
```

```{card}
:header: **Greengenes 13_8 99% OTUs full-length sequences**

**Download**: [Greengenes 13_8 99% OTUs full-length sequences](https://data.qiime2.org/2020.2/common/gg-13-8-99-nb-classifier.qza)\
**UUID**: 2475458d-db2d-46d8-938e-269d5c548225\
**SHA256**: a106451cc4719cde56141a7124219da6ba6e44eab15e02db306e486063c85a35\
**Sklearn Version**: 0.22.1\
**Date Trained**: 2020-02-17\
**Notes**: N/A\
**Citations**: @McDonald2023-gq, @Bokulich2018-yb
```

```{card}
:header: **Greengenes 13_8 99% OTUs from 515F/806R region of sequences**

**Download**: [Greengenes 13_8 99% OTUs from 515F/806R region of sequences](https://data.qiime2.org/2020.2/common/gg-13-8-99-515-806-nb-classifier.qza)\
**UUID**: 18d34bd0-8e7e-4af6-ba34-a31c03fceb70\
**SHA256**: 3d64bc343c5d364302b6440d6d426a18583297edf17dc144ca21ca2c4f23ce18\
**Sklearn Version**: 0.22.1\
**Date Trained**: 2020-02-17\
**Notes**: N/A\
**Citations**: @McDonald2023-gq, @Bokulich2018-yb
```

(Silva)=
:::{note}
:header: Note

The Silva classifiers provided here include species-level taxonomy. While Silva annotations do include species, Silva does not curate the species-level taxonomy so this information may be unreliable.
In a future version of QIIME 2 we will no longer include species-level information in our Silva taxonomy classifiers.
This is discussed on the QIIME 2 Forum [here](https://forum.qiime2.org/t/processing-filtering-and-evaluating-the-silva-database-and-other-reference-sequence-data-with-rescript/15494#heading--second-header) (see Species-labels: caveat emptor!).
:::

(GG2)=
:::{note}
:header: Note

Greengenes2 has succeeded Greengenes 13_8.
If you still need to access the outdated 13_8 classifiers, for example to reproduce old results or to compare against new classifiers, you can access them through older QIIME 2 versions.
:::

(Silva-Citations)=
:::{note}
See the [SILVA website](https://www.arb-silva.de/) for the latest citation information for this reference database.
:::

```{image} ./static/images/qiime2-resources-ai-art.png
:alt: Qiime2 Resources AI Art
:align: left
```
