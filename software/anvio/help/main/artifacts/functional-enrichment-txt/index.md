---
layout: page
title: functional-enrichment-txt [artifact]
categories: [anvio]
comments: false
redirect_from: /m/functional-enrichment-txt
image:
  featurerelative: ../../../images/header.png
  display: true
---


{% include _toc.html %}


<img src="../../images/icons/TXT.png" alt="TXT" style="width:100px; border:none" />

A TXT-type anvi'o artifact. This artifact is typically generated, used, and/or exported **by anvi'o** (and not provided by the user)..

Back to the **[main page](../../)** of anvi'o programs and artifacts.

## Provided by


<p style="text-align: left" markdown="1"><span class="artifact-p">[anvi-compute-functional-enrichment](../../programs/anvi-compute-functional-enrichment)</span> <span class="artifact-p">[anvi-display-functions](../../programs/anvi-display-functions)</span></p>


## Required or used by


There are no anvi'o tools that use or require this artifact directly, which means it is most likely an end-product for the user.


## Description

This is a TAB-delimited output file that describes enrichment scores and associated groups for functions or metabolic modules in groups of genomes or samples. It is produced by <span class="artifact-n">[anvi-compute-functional-enrichment](/software/anvio/help/main/programs/anvi-compute-functional-enrichment)</span>.

## General format

Each row in the matrix describes an entity (a function, functional association of a gene cluster, or metabolic module) that is associated with one or more groups of samples or genomes. These are listed with the highest enrichment scores displayed first.

The following columns of information are listed in the file:

- the name of the enriched entity, which can be a functional association, metabolic module, or function. The header of this column is either your functional annotation source, OR 'KEGG_MODULE' if you are working with metabolic modules
- enrichment_score: a measure of much this particular entity is enriched in the group it is associated with (i.e., measures how unique this entity [see column 1] is to this group(s) [see column 5])
- unadjusted_p_value: the significance value of the hypothesis test for enrichment, unadjusted for multiple hypothesis testing
- adjusted_q_value: the adjusted p-value after taking into account multiple hypothesis testing
- associated groups: the list of groups that this entity is associated with
- accession: a function accession number or KEGG module number (depends on your input option for <span class="artifact-n">[anvi-compute-functional-enrichment](/software/anvio/help/main/programs/anvi-compute-functional-enrichment)</span>)
- a list of gene cluster ids, sample names, or genome names that this entity is found in (also depends on your input option for <span class="artifact-n">[anvi-compute-functional-enrichment](/software/anvio/help/main/programs/anvi-compute-functional-enrichment)</span>)
- p values for each group: gives the proportion of the group's member genomes or samples in which this entity was found.
- N values for each group: gives the total number of genomes or samples in each group.

## A specific example - enriched functions in pangenomes

When you run <span class="artifact-n">[anvi-compute-functional-enrichment](/software/anvio/help/main/programs/anvi-compute-functional-enrichment)</span> (with input option 1) to compute enrichment scores for functions in a pangenome, the resulting matrix describes the gene cluster-level functional associations that are enriched within specific groups of your pangenome. This is described in more detail [in the pangenomics tutorial](http://merenlab.org/2016/11/08/pangenomics-v2/#making-sense-of-functions-in-your-pangenome).

Here is a more concrete example (the same example as in the [pangenomics tutorial](http://merenlab.org/2016/11/08/pangenomics-v2/#making-sense-of-functions-in-your-pangenome)). Note that that tutorial uses `COG_FUNCTION` as the functional annotation source, and has `LL` (low light) and `HL` (high light) as the two pan-groups.

|COG_FUNCTION | enrichment_score | unadjusted_p_value | adjusted_q_value | associated_groups | accession | gene_clusters_ids | p_LL | p_HL | N_LL | N_HL|
|-- | -- | -- | -- | -- | -- | -- | -- | -- | --| --|
|Proteasome lid subunit RPN8/RPN11, contains Jab1/MPN domain metalloenzyme (JAMM) motif | 31.00002279 | 2.58E-08 | 1.43E-06 | LL | COG1310 | GC_00002219, GC_00003850, GC_00004483 | 1 | 0 | 11 | 20|
|Adenine-specific DNA glycosylase, acts on AG and A-oxoG pairs | 31.00002279 | 2.58E-08 | 1.43E-06 | LL | COG1194 | GC_00001711 | 1 | 0 | 11 | 20|
|Periplasmic beta-glucosidase and related glycosidases | 31.00002279 | 2.58E-08 | 1.43E-06 | LL | COG1472 | GC_00002086, GC_00003909 | 1 | 0 | 11 | 20|
|Single-stranded DNA-specific exonuclease, DHH superfamily, may be involved in archaeal DNA replication intiation | 31.00002279 | 2.58E-08 | 1.43E-06 | LL | COG0608 | GC_00002752, GC_00003786, GC_00004838, GC_00007241 | 1 | 0 | 11 | 20|
|Ser/Thr protein kinase RdoA involved in Cpx stress response, MazF antagonist | 31.00002279 | 2.58E-08 | 1.43E-06 | LL | COG2334 | GC_00002783, GC_00003936, GC_00004631, GC_00005468 | 1 | 0 | 11 | 20|
|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|
|Signal transduction histidine kinase | -7.34E-41 | 1 | 1 | NA | COG5002 | GC_00000773, GC_00004293 | 1 | 1 | 11 | 20|
|tRNA A37 methylthiotransferase MiaB | -7.34E-41 | 1 | 1 | NA | COG0621 | GC_00000180, GC_00000851 | 1 | 1 | 11 | 20|


{:.notice}
Edit [this file](https://github.com/merenlab/anvio/tree/master/anvio/docs/artifacts/functional-enrichment-txt.md) to update this information.

