---
layout: page
title: anvi-import-functions [program]
categories: [anvio]
comments: false
redirect_from: /m/anvi-import-functions
image:
  featurerelative: ../../../images/header.png
  display: true
---

Parse and store functional annotation of genes.

See **[program help menu](../../../../vignette#anvi-import-functions)** or go back to the **[main page](../../)** of anvi'o programs and artifacts.


{% include _toc.html %}
<div id="svg" class="subnetwork"></div>
{% capture network_path %}{{ "network.json" }}{% endcapture %}
{% capture network_height %}{{ 300 }}{% endcapture %}
{% include _project-anvio-graph.html %}


## Can provide

<p style="text-align: left" markdown="1"><span class="artifact-p">[functions](../../artifacts/functions) <img src="../../images/icons/CONCEPT.png" class="artifact-icon-mini" /></span></p>

## Can consume

<p style="text-align: left" markdown="1"><span class="artifact-r">[contigs-db](../../artifacts/contigs-db) <img src="../../images/icons/DB.png" class="artifact-icon-mini" /></span> <span class="artifact-r">[functions-txt](../../artifacts/functions-txt) <img src="../../images/icons/TXT.png" class="artifact-icon-mini" /></span></p>

## Usage


This program **takes in a <span class="artifact-n">[functions-txt](/software/anvio/help/main/artifacts/functions-txt)</span> to annotate your <span class="artifact-n">[contigs-db](/software/anvio/help/main/artifacts/contigs-db)</span> with <span class="artifact-n">[functions](/software/anvio/help/main/artifacts/functions)</span>.** Basically, if you have already have the gene functions for the contigs in your <span class="artifact-n">[contigs-db](/software/anvio/help/main/artifacts/contigs-db)</span> available in a file, you can import them into anvi'o using this command. 

You can find a really comprehesive walkthrough of this program on [this blog post about importing functions](http://merenlab.org/2016/06/18/importing-functions/), including information about built-in anvi'o parsers for InterProScan and the EggNOG database.

If you want to overwrite any function annotations you already have, just add the tag `--drop-previous-annotations`. 



{:.notice}
Edit [this file](https://github.com/merenlab/anvio/tree/master/anvio/docs/programs/anvi-import-functions.md) to update this information.


## Additional Resources


* [Importing functions](http://merenlab.org/2016/06/18/importing-functions/)

* [Importing GhostKOALA/KEGG annotations](http://merenlab.org/2018/01/17/importing-ghostkoala-annotations/)

* [Importing VirSorter phage annotaions](http://merenlab.org/2018/02/08/importing-virsorter-annotations/)


{:.notice}
Are you aware of resources that may help users better understand the utility of this program? Please feel free to edit [this file](https://github.com/merenlab/anvio/tree/master/bin/anvi-import-functions) on GitHub. If you are not sure how to do that, find the `__resources__` tag in [this file](https://github.com/merenlab/anvio/blob/master/bin/anvi-interactive) to see an example.
