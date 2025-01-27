---
layout: page
title: anvi-export-splits-taxonomy [program]
categories: [anvio]
comments: false
image:
  featurerelative: ../../../images/header.png
  display: true
---

Export taxonomy for splits found in an anvi&#x27;o contigs database.

See **[program help menu](../../../../vignette#anvi-export-splits-taxonomy)** or go back to the **[main page](../../)** of anvi'o programs and artifacts.


{% include _toc.html %}
<div id="svg" class="subnetwork"></div>
{% capture network_path %}{{ "network.json" }}{% endcapture %}
{% capture network_height %}{{ 300 }}{% endcapture %}
{% include _project-anvio-graph.html %}


## Can provide

<p style="text-align: left" markdown="1"><span class="artifact-p">[splits-taxonomy-txt](../../artifacts/splits-taxonomy-txt) <img src="../../images/icons/TXT.png" class="artifact-icon-mini" /></span></p>

## Can consume

<p style="text-align: left" markdown="1"><span class="artifact-r">[contigs-db](../../artifacts/contigs-db) <img src="../../images/icons/DB.png" class="artifact-icon-mini" /></span></p>

## Usage


This program exports the taxonomy hits for the splits contained in a <span class="artifact-n">[contigs-db](/software/anvio/help/7/artifacts/contigs-db)</span>, outputting them in a <span class="artifact-n">[splits-taxonomy-txt](/software/anvio/help/7/artifacts/splits-taxonomy-txt)</span>. 

To do this, anvi'o examines all of the annotated genes within your splits and returns the taxon ID with the most genes associated with it. For example, a split with 3 genes identified as E. coli, 2 genes identified as Staphylococcus aureus, and 1 as Streptococcus pneumoniae would be annotated as E. coli. 

To run this program, just provide a <span class="artifact-n">[contigs-db](/software/anvio/help/7/artifacts/contigs-db)</span>:

<div class="codeblock" markdown="1">
anvi&#45;export&#45;splits&#45;taxonomy &#45;c <span class="artifact&#45;n">[contigs&#45;db](/software/anvio/help/7/artifacts/contigs&#45;db)</span> \
                            &#45;o PATH/TO/<span class="artifact&#45;n">[splits&#45;taxonomy&#45;txt](/software/anvio/help/7/artifacts/splits&#45;taxonomy&#45;txt)</span>

</div>


{:.notice}
Edit [this file](https://github.com/merenlab/anvio/tree/master/anvio/docs/programs/anvi-export-splits-taxonomy.md) to update this information.


## Additional Resources



{:.notice}
Are you aware of resources that may help users better understand the utility of this program? Please feel free to edit [this file](https://github.com/merenlab/anvio/tree/master/bin/anvi-export-splits-taxonomy) on GitHub. If you are not sure how to do that, find the `__resources__` tag in [this file](https://github.com/merenlab/anvio/blob/master/bin/anvi-interactive) to see an example.
