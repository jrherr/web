---
layout: page
title: anvi-convert-trnaseq-database [program]
categories: [anvio]
comments: false
image:
  featurerelative: ../../../images/header.png
  display: true
---

A program that processes one or more anvio&#x27; tRNA-seq databases generated by `anvi-trnaseq` to generate anvi&#x27;o contigs and merged profile databases that are accessible to the rest of the tools in anvi&#x27;o software ecosystem. Briefly, this program will determine final seed sequences from input tRNA-seq databases, determine their coverages across samples, identify tRNA modification sites, and INDELs associated with transcripts in each sample against the seed sequences and store all these data into resulting databases for interactive visualization of the data or in-depth analysis using other anvi&#x27;o frameworks.

See **[program help menu](../../../../vignette#anvi-convert-trnaseq-database)** or go back to the **[main page](../../)** of anvi'o programs and artifacts.


{% include _toc.html %}
<div id="svg" class="subnetwork"></div>
{% capture network_path %}{{ "network.json" }}{% endcapture %}
{% capture network_height %}{{ 300 }}{% endcapture %}
{% include _project-anvio-graph.html %}


## Can provide

<p style="text-align: left" markdown="1"><span class="artifact-p">[contigs-db](../../artifacts/contigs-db) <img src="../../images/icons/DB.png" class="artifact-icon-mini" /></span> <span class="artifact-p">[profile-db](../../artifacts/profile-db) <img src="../../images/icons/DB.png" class="artifact-icon-mini" /></span></p>

## Can consume

<p style="text-align: left" markdown="1"><span class="artifact-r">[trnaseq-db](../../artifacts/trnaseq-db) <img src="../../images/icons/DB.png" class="artifact-icon-mini" /></span></p>

## Usage


This program converts one or more <span class="artifact-n">[trnaseq-db](/software/anvio/help/7/artifacts/trnaseq-db)</span>s into a <span class="artifact-n">[contigs-db](/software/anvio/help/7/artifacts/contigs-db)</span> and <span class="artifact-n">[profile-db](/software/anvio/help/7/artifacts/profile-db)</span>, forming tRNA seed sequences in the process.

After <span class="artifact-n">[anvi-trnaseq](/software/anvio/help/7/programs/anvi-trnaseq)</span> is run on a set of samples (or sample splits) from an experiment, the resulting sample databases are analyzed by this program. The <span class="artifact-n">[contigs-db](/software/anvio/help/7/artifacts/contigs-db)</span> and <span class="artifact-n">[profile-db](/software/anvio/help/7/artifacts/profile-db)</span> generated by this program can be displayed and analyzed like other 'omics data in anvi'o.

As with <span class="artifact-n">[anvi-trnaseq](/software/anvio/help/7/programs/anvi-trnaseq)</span>, we encourage you to read through the options in the `anvi-convert-trnaseq-database --help` menu, since the various analyses occurring within this program can be manipulated by the user. Most of the heavy lifting occurred in <span class="artifact-n">[anvi-trnaseq](/software/anvio/help/7/programs/anvi-trnaseq)</span>, meaning that `anvi-convert-trnaseq-database` can easily be run multiple times in a matter of minutes to find, for example, the appropriate number of tRNA seed sequences to display (by adjusting `--max-reported-trna-seeds`) and the necessary coverage cutoffs to isolate positions with modified nucleotides from unfiltered single nucleotide variants (by adjusting `--min-third-fourth-nt`).


### Convert two samples

<div class="codeblock" markdown="1">
anvi&#45;convert&#45;trnaseq&#45;database example_trnaseq_database_1 example_trnaseq_database_2 \
                              &#45;o example_empty_output_directory_path
                              &#45;n example_project_name
</div>

### Convert two sample splits, assigning priority to the demethylase split in calling the underlying nucleotide at modified positions

<div class="codeblock" markdown="1">
anvi&#45;convert&#45;trnaseq&#45;database example_untreated_trnaseq_database example_demethylase_trnaseq_database \
                              &#45;o example_empty_output_directory_path
                              &#45;n example_project_name
                              &#45;&#45;preferred&#45;treatment demethylase
</div>


{:.notice}
Edit [this file](https://github.com/merenlab/anvio/tree/master/anvio/docs/programs/anvi-convert-trnaseq-database.md) to update this information.


## Additional Resources



{:.notice}
Are you aware of resources that may help users better understand the utility of this program? Please feel free to edit [this file](https://github.com/merenlab/anvio/tree/master/bin/anvi-convert-trnaseq-database) on GitHub. If you are not sure how to do that, find the `__resources__` tag in [this file](https://github.com/merenlab/anvio/blob/master/bin/anvi-interactive) to see an example.
