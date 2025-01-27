---
layout: page
title: anvi-script-filter-hmm-hits-table [program]
categories: [anvio]
comments: false
redirect_from: /m/anvi-script-filter-hmm-hits-table
image:
  featurerelative: ../../../images/header.png
  display: true
---

Add or remove entries in a contigDB hmm_hits table..

See **[program help menu](../../../../vignette#anvi-script-filter-hmm-hits-table)** or go back to the **[main page](../../)** of anvi'o programs and artifacts.


{% include _toc.html %}
<div id="svg" class="subnetwork"></div>
{% capture network_path %}{{ "network.json" }}{% endcapture %}
{% capture network_height %}{{ 300 }}{% endcapture %}
{% include _project-anvio-graph.html %}


## Can provide

<p style="text-align: left" markdown="1"><span class="artifact-p">[contigs-db](../../artifacts/contigs-db) <img src="../../images/icons/DB.png" class="artifact-icon-mini" /></span> <span class="artifact-p">[hmm-hits](../../artifacts/hmm-hits) <img src="../../images/icons/CONCEPT.png" class="artifact-icon-mini" /></span></p>

## Can consume

<p style="text-align: left" markdown="1"><span class="artifact-r">[contigs-db](../../artifacts/contigs-db) <img src="../../images/icons/DB.png" class="artifact-icon-mini" /></span> <span class="artifact-r">[hmm-source](../../artifacts/hmm-source) <img src="../../images/icons/HMM.png" class="artifact-icon-mini" /></span> <span class="artifact-r">[hmm-hits](../../artifacts/hmm-hits) <img src="../../images/icons/CONCEPT.png" class="artifact-icon-mini" /></span></p>

## Usage


This program is for filtering a <span class="artifact-n">[hmm-source](/software/anvio/help/main/artifacts/hmm-source)</span> from a <span class="artifact-n">[hmm-hits](/software/anvio/help/main/artifacts/hmm-hits)</span> in a <span class="artifact-n">[contigs-db](/software/anvio/help/main/artifacts/contigs-db)</span> using HMM alignment parameters such as query-coverage and target-coverage. Briefly, the program will remove all records from an <span class="artifact-n">[hmm-source](/software/anvio/help/main/artifacts/hmm-source)</span> in the <span class="artifact-n">[hmm-hits](/software/anvio/help/main/artifacts/hmm-hits)</span> then import a new <span class="artifact-n">[hmm-hits](/software/anvio/help/main/artifacts/hmm-hits)</span> table into the <span class="artifact-n">[contigs-db](/software/anvio/help/main/artifacts/contigs-db)</span> that was filtered to your specifications. At the moment, this tool is only designed to work with `hmmsearch` with protein sequences. The `--domtblout` can be produced from running `anvi-run-hmms` with your <span class="artifact-n">[hmm-source](/software/anvio/help/main/artifacts/hmm-source)</span> of interest and using the `--domtblout` parameter AND  `hmmsearch` as the program.

To list available <span class="artifact-n">[hmm-source](/software/anvio/help/main/artifacts/hmm-source)</span> in a database:

<div class="codeblock" markdown="1">
anvi&#45;script&#45;filter&#45;hmm&#45;hit&#45;table &#45;c <span class="artifact&#45;n">[contigs&#45;db](/software/anvio/help/main/artifacts/contigs&#45;db)</span> \
                                 &#45;&#45;list&#45;hmm&#45;sources
</div>

Make `--domtblout` with `anvi-run-hmms`

<div class="codeblock" markdown="1">
anvi&#45;run&#45;hmms &#45;c <span class="artifact&#45;n">[contigs&#45;db](/software/anvio/help/main/artifacts/contigs&#45;db)</span> \
              &#45;I Bacteria_71 \
              &#45;&#45;just&#45;do&#45;it \
              &#45;&#45;hmmer&#45;program hmmsearch \
              &#45;&#45;hmm&#45;domain&#45;tblout&#45;path hmmsearch
</div>

Then you can filter out hits using query or target coverage! Here's an example where we can filter out hmm_hits with a target-coverage less than 90%:

<div class="codeblock" markdown="1">
anvi&#45;script&#45;filter&#45;hmm&#45;hit&#45;table &#45;c <span class="artifact&#45;n">[contigs&#45;db](/software/anvio/help/main/artifacts/contigs&#45;db)</span> \
                                 &#45;&#45;hmm&#45;source <span class="artifact&#45;n">[hmm&#45;source](/software/anvio/help/main/artifacts/hmm&#45;source)</span> \
                                 &#45;&#45;domtblout hmmsearch_domtable \
                                 &#45;&#45;target&#45;coverage 0.9
</div>


{:.notice}
Edit [this file](https://github.com/merenlab/anvio/tree/master/anvio/docs/programs/anvi-script-filter-hmm-hits-table.md) to update this information.


## Additional Resources



{:.notice}
Are you aware of resources that may help users better understand the utility of this program? Please feel free to edit [this file](https://github.com/merenlab/anvio/tree/master/bin/anvi-script-filter-hmm-hits-table) on GitHub. If you are not sure how to do that, find the `__resources__` tag in [this file](https://github.com/merenlab/anvio/blob/master/bin/anvi-interactive) to see an example.
