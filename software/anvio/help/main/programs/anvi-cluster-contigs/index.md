---
layout: page
title: anvi-cluster-contigs [program]
categories: [anvio]
comments: false
redirect_from: /m/anvi-cluster-contigs
image:
  featurerelative: ../../../images/header.png
  display: true
---

A program to cluster items in a merged anvi&#x27;o profile using automatic binning algorithms.

See **[program help menu](../../../../vignette#anvi-cluster-contigs)** or go back to the **[main page](../../)** of anvi'o programs and artifacts.


{% include _toc.html %}
<div id="svg" class="subnetwork"></div>
{% capture network_path %}{{ "network.json" }}{% endcapture %}
{% capture network_height %}{{ 300 }}{% endcapture %}
{% include _project-anvio-graph.html %}


## Can provide

<p style="text-align: left" markdown="1"><span class="artifact-p">[collection](../../artifacts/collection) <img src="../../images/icons/COLLECTION.png" class="artifact-icon-mini" /></span> <span class="artifact-p">[bin](../../artifacts/bin) <img src="../../images/icons/BIN.png" class="artifact-icon-mini" /></span></p>

## Can consume

<p style="text-align: left" markdown="1"><span class="artifact-r">[profile-db](../../artifacts/profile-db) <img src="../../images/icons/DB.png" class="artifact-icon-mini" /></span> <span class="artifact-r">[contigs-db](../../artifacts/contigs-db) <img src="../../images/icons/DB.png" class="artifact-icon-mini" /></span> <span class="artifact-r">[collection](../../artifacts/collection) <img src="../../images/icons/COLLECTION.png" class="artifact-icon-mini" /></span></p>

## Usage


This program clusters the contigs stored in a <span class="artifact-n">[profile-db](/software/anvio/help/main/artifacts/profile-db)</span> using your binning algorithm of choice and stores the results in several <span class="artifact-n">[bin](/software/anvio/help/main/artifacts/bin)</span>s. 

This is a quick alternative to manually binning your contigs, but it might miss some details that a human doing manual binning would find. After running this, you might want to run <span class="artifact-n">[anvi-summarize](/software/anvio/help/main/programs/anvi-summarize)</span> on the resulting <span class="artifact-n">[collection](/software/anvio/help/main/artifacts/collection)</span> to look through your bins, and, if necessary, use <span class="artifact-n">[anvi-refine](/software/anvio/help/main/programs/anvi-refine)</span> to change the contents of them. 

You have to option to use several different clustering algorithms, which you'll specify with the `driver` parameter: [concoct](https://github.com/BinPro/CONCOCT/blob/develop/doc/source/index.rst), [metabat2](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6662567/), [maxbin2](https://academic.oup.com/bioinformatics/article/32/4/605/1744462), [dastool](https://github.com/cmks/DAS_Tool), and [binsanity](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5345454/). 

So, a run of this program will look like the following:

<div class="codeblock" markdown="1">
anvi&#45;cluster&#45;contigs &#45;p <span class="artifact&#45;n">[profile&#45;db](/software/anvio/help/main/artifacts/profile&#45;db)</span> \
                     &#45;c <span class="artifact&#45;n">[contigs&#45;db](/software/anvio/help/main/artifacts/contigs&#45;db)</span> \ 
                     &#45;C <span class="artifact&#45;n">[collection](/software/anvio/help/main/artifacts/collection)</span> \ 
                     &#45;&#45;driver concoct
</div>

Once you specify an algorithm, there are many algorithm specific parameters that you can change to your liking. When this program is set up, these parameters will appear in the help menu for the algorithms that anvi'o can find. 


{:.notice}
Edit [this file](https://github.com/merenlab/anvio/tree/master/anvio/docs/programs/anvi-cluster-contigs.md) to update this information.


## Additional Resources



{:.notice}
Are you aware of resources that may help users better understand the utility of this program? Please feel free to edit [this file](https://github.com/merenlab/anvio/tree/master/bin/anvi-cluster-contigs) on GitHub. If you are not sure how to do that, find the `__resources__` tag in [this file](https://github.com/merenlab/anvio/blob/master/bin/anvi-interactive) to see an example.
