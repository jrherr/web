---
layout: page
title: anvi-script-calculate-pn-ps-ratio [program]
categories: [anvio]
comments: false
redirect_from: /m/anvi-script-calculate-pn-ps-ratio
image:
  featurerelative: ../../../images/header.png
  display: true
---

FIXME.

See **[program help menu](../../../../vignette#anvi-script-calculate-pn-ps-ratio)** or go back to the **[main page](../../)** of anvi'o programs and artifacts.


{% include _toc.html %}
<div id="svg" class="subnetwork"></div>
{% capture network_path %}{{ "network.json" }}{% endcapture %}
{% capture network_height %}{{ 300 }}{% endcapture %}
{% include _project-anvio-graph.html %}


## Can provide

<p style="text-align: left" markdown="1"><span class="artifact-p">[pn-ps-data](../../artifacts/pn-ps-data) <img src="../../images/icons/CONCEPT.png" class="artifact-icon-mini" /></span></p>

## Can consume

<p style="text-align: left" markdown="1"><span class="artifact-r">[contigs-db](../../artifacts/contigs-db) <img src="../../images/icons/DB.png" class="artifact-icon-mini" /></span> <span class="artifact-r">[variability-profile-txt](../../artifacts/variability-profile-txt) <img src="../../images/icons/TXT.png" class="artifact-icon-mini" /></span></p>

## Usage


This program **calculates the pN/pS ratio** for each gene in a <span class="artifact-n">[contigs-db](/software/anvio/help/main/artifacts/contigs-db)</span> and outputs it as a <span class="artifact-n">[pn-ps-data](/software/anvio/help/main/artifacts/pn-ps-data)</span> artifact.

### What is the pN/pS ratio?

The pN/pS ratio (first described in [Schloissnig et al. 2012](https://doi.org/10.1038/nature11711))
is the ratio of 2 rates: the rates of non-synonymous (pN) and synonymous (pS) **polymorphism**. It is analogous to
dN/dS, which is the ratio of rates between non-synonymous (dN) and synonymous **substitutions** between 2
strains/species. We calculate pN/pS from allele frequency obtained through SCVs and SAAVs (see
[publication in preparation](FIXME)) for exact implementation details.

### Neat. How do I use this program?

Firstly, you'll need to run <span class="artifact-n">[anvi-gen-variability-profile](/software/anvio/help/main/programs/anvi-gen-variability-profile)</span> using the flag `--engine CDN` to get a <span class="artifact-n">[variability-profile-txt](/software/anvio/help/main/artifacts/variability-profile-txt)</span> for SCVs (single codon variants), which we'll name `SCVs.txt` in this example.

Then you can run this program like so:

<div class="codeblock" markdown="1">
anvi&#45;script&#45;calculate&#45;pn&#45;ps&#45;ratio &#45;V SCVs.txt \
                                  &#45;c <span class="artifact&#45;n">[contigs&#45;db](/software/anvio/help/main/artifacts/contigs&#45;db)</span> \
                                  &#45;o output_dir 
</div>

A pN/pS value is calculated for each (gene, sample) combo. This will result in a directory called `output_dir` that contains several tables that describe each of your genes. See <span class="artifact-n">[pn-ps-data](/software/anvio/help/main/artifacts/pn-ps-data)</span> for more information.

### Other parameters

This program has some default filtering choices that you should pay mind to. You can tune these filter options with the following variables:

- The minimum departure from consensus for a variable position (`--min-departure-from-consensus`).
- The minimum departure from reference for a variable position (`--min-departure-from-reference`).
- The minimum number of SCVs in a grouping (`--minimum-num-variants`).
- The minimum coverage at a variable position (`--min-coverage`).


{:.notice}
Edit [this file](https://github.com/merenlab/anvio/tree/master/anvio/docs/programs/anvi-script-calculate-pn-ps-ratio.md) to update this information.


## Additional Resources



{:.notice}
Are you aware of resources that may help users better understand the utility of this program? Please feel free to edit [this file](https://github.com/merenlab/anvio/tree/master/bin/anvi-script-calculate-pn-ps-ratio) on GitHub. If you are not sure how to do that, find the `__resources__` tag in [this file](https://github.com/merenlab/anvio/blob/master/bin/anvi-interactive) to see an example.
