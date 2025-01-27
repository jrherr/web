---
layout: page
title: linkmers-txt [artifact]
categories: [anvio]
comments: false
image:
  featurerelative: ../../../images/header.png
  display: true
---


{% include _toc.html %}


<img src="../../images/icons/TXT.png" alt="TXT" style="width:100px; border:none" />

A TXT-type anvi'o artifact. This artifact is typically provided **by the user** for anvi'o to import into its databases, process, and/or use.

Back to the **[main page](../../)** of anvi'o programs and artifacts.

## Provided by


<p style="text-align: left" markdown="1"><span class="artifact-p">[anvi-report-linkmers](../../programs/anvi-report-linkmers)</span> <span class="artifact-p">[anvi-script-transpose-matrix](../../programs/anvi-script-transpose-matrix)</span></p>


## Required or used by


<p style="text-align: left" markdown="1"><span class="artifact-r">[anvi-oligotype-linkmers](../../programs/anvi-oligotype-linkmers)</span> <span class="artifact-r">[anvi-script-transpose-matrix](../../programs/anvi-script-transpose-matrix)</span></p>


## Description

This is a tab-delimited table where each row represents a a short read that mapped to a specific position in a reference contig. This is the output of <span class="artifact-n">[anvi-report-linkmers](/software/anvio/help/7/programs/anvi-report-linkmers)</span>, where those reference positions are given by the user.

For instance, if <span class="artifact-n">[anvi-report-linkmers](/software/anvio/help/7/programs/anvi-report-linkmers)</span> was run on three samples (`SAMPLE-01.bam`, `SAMPLE-02.bam`, and `SAMPLE-03.bam`) with this contigs-and-positions file,

<table>
  <tbody>
    <tr>
      <td> contig_1720 </td>
      <td> 7111,7115,7120 </td>
    </tr>
  </tbody>
</table>

Then the output would be the following: 

|entry_id|sample_id|request_id|contig_name|pos_in_contig|pos_in_read|base|read_unique_id|read_X|reverse|sequence|
|:--|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--|
|000000001|SAMPLE-01|001|contig_1720|7111|160|G|bc3aa6b95ce110067|read-2|True|ATTGGTTTTGCTATTGGGTTTGTCGTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTA|
|000000002|SAMPLE-01|001|contig_1720|7111|160|G|156295ff5928fc055|read-2|True|ATTGGTTTTGCTATTGGGTTTGTCGTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTT|
|000000003|SAMPLE-01|001|contig_1720|7111|141|G|7a8947678111bb905|read-2|True|TTGTCGTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACA|
|000000004|SAMPLE-01|001|contig_1720|7111|135|A|2a3de408930252949|read-2|False|TGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTAGGAGTGTTT|
|000000005|SAMPLE-01|001|contig_1720|7111|130|G|5f995d129fdabe64f|read-2|True|ATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATT|
|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|
|000000033|SAMPLE-01|001|contig_1720|7115|164|A|bc3aa6b95ce110067|read-2|True|ATTGGTTTTGCTATTGGGTTTGTCGTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTA|
|000000034|SAMPLE-01|001|contig_1720|7115|164|A|156295ff5928fc055|read-2|True|ATTGGTTTTGCTATTGGGTTTGTCGTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTT|
|000000035|SAMPLE-01|001|contig_1720|7115|145|A|7a8947678111bb905|read-2|True|TTGTCGTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACA|
|000000036|SAMPLE-01|001|contig_1720|7115|139|G|2a3de408930252949|read-2|False|TGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTAGGAGTGTTT|
|000000064|SAMPLE-01|001|contig_1720|7115|16|A|28a3a440fda5142b9|read-2|True|AGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAGTTATGGCTTATAGTGGTAATAGTAATTTACCGGGAAGTGCAATAATTATTATTTTTGTACCGGTAATGTTAGGAATTATCTATTTAGCTAGTAAGGGTGTGGTTAAA|
|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|
|000000065|SAMPLE-01|001|contig_1720|7120|169|T|bc3aa6b95ce110067|read-2|True|ATTGGTTTTGCTATTGGGTTTGTCGTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTA|
|000000066|SAMPLE-01|001|contig_1720|7120|169|T|156295ff5928fc055|read-2|True|ATTGGTTTTGCTATTGGGTTTGTCGTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTT|
|000000067|SAMPLE-01|001|contig_1720|7120|150|T|7a8947678111bb905|read-2|True|TTGTCGTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACA|
|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|
|000000097|SAMPLE-02|001|contig_1720|7111|140|G|ddb72ab632d753591|read-2|True|TGTCGTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCA|
|000000098|SAMPLE-02|001|contig_1720|7111|75|G|e7506ec6da1f08697|read-2|False|TAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAGTTATGGCTTATAGTGGTAATAGTAATTTACCGGGAAGTGCA|
|000000099|SAMPLE-02|001|contig_1720|7111|65|G|07f926c7d8dd57e03|read-2|True|TCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAGTTATGGCTTATAGTGGTAATAGTAATTTACCGGGAAGTGCAATAATTATTATTTTTGTACC|
|000000100|SAMPLE-02|001|contig_1720|7111|54|G|97fb9b743bbe5d89a|read-2|True|GTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAGTTATGGCTTATAGTGGTAATAGTAATTTACCGGGAAGTGCAATAATTATTATTTTTGTACCGGTAATGTTA|
|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|
|000000103|SAMPLE-02|001|contig_1720|7115|69|A|07f926c7d8dd57e03|read-2|True|TCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAGTTATGGCTTATAGTGGTAATAGTAATTTACCGGGAAGTGCAATAATTATTATTTTTGTACC|
|000000104|SAMPLE-02|001|contig_1720|7115|58|A|97fb9b743bbe5d89a|read-2|True|GTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAGTTATGGCTTATAGTGGTAATAGTAATTTACCGGGAAGTGCAATAATTATTATTTTTGTACCGGTAATGTTA|
|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|
|000000105|SAMPLE-02|001|contig_1720|7120|149|T|ddb72ab632d753591|read-2|True|TGTCGTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCA|
|000000106|SAMPLE-02|001|contig_1720|7120|84|T|e7506ec6da1f08697|read-2|False|TAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAGTTATGGCTTATAGTGGTAATAGTAATTTACCGGGAAGTGCA|
|000000107|SAMPLE-02|001|contig_1720|7120|74|T|07f926c7d8dd57e03|read-2|True|TCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAGTTATGGCTTATAGTGGTAATAGTAATTTACCGGGAAGTGCAATAATTATTATTTTTGTACC|
|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|
|000000109|SAMPLE-03|001|contig_1720|7111|181|G|5b30beaad5028d9be|read-2|False|CATCATAGTAATATTGCAACTATTGGTTTTGCTATTGGGTTTGTCGTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTT|
|000000110|SAMPLE-03|001|contig_1720|7111|167|G|a74a16460eee34549|read-2|False|TGCAACTATTGGTTTTGCTATTGGGTTTGTCGTGATGATGATGATAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTT|
|000000111|SAMPLE-03|001|contig_1720|7111|158|G|3ec0b8a88b8cf6f6b|read-2|False|TGGTTTTGCTATTGGGTTTGTCGTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTA|
|000000112|SAMPLE-03|001|contig_1720|7111|158|G|237828c6637b1648e|read-2|False|TGGTTTTGCTATTGGGTTTGTCGGGATGATGATGTTAGATGTCGCCTTAGGTTAATCTGTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTA|
|000000113|SAMPLE-03|001|contig_1720|7111|154|G|006dfcf9742b2a323|read-2|True|TTTGCTATTGGGTTTGTCGTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGATGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTA|
|000000114|SAMPLE-03|001|contig_1720|7111|153|G|ab174bde7a9f86013|read-2|False|TTGCTATTGGGTTTGTCGTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAA|
|000000115|SAMPLE-03|001|contig_1720|7111|150|G|4fdd1e6de2a10c923|read-2|True|CTATTGGGTTTGTCGTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTT|
|000000116|SAMPLE-03|001|contig_1720|7111|149|G|cc5f916935b4b42be|read-2|False|TATTGGGTTTTTCGTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAA|
|000000117|SAMPLE-03|001|contig_1720|7111|148|G|857199a218edef55d|read-2|False|ATTGGGTTTGTCGTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACGGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTT|
|000000118|SAMPLE-03|001|contig_1720|7111|147|G|7f5890d7daeb66d06|read-2|False|TTGGGTTTGTCGTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAA|
|000000119|SAMPLE-03|001|contig_1720|7111|145|G|e1f31dfa0435ffb78|read-2|True|GGGTTTGTCGTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAATAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTT|
|000000120|SAMPLE-03|001|contig_1720|7111|143|G|8204d0adc702d99ba|read-2|True|GTTTGTCGTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAA|
|000000121|SAMPLE-03|001|contig_1720|7111|142|G|baaa46d85f2425750|read-2|False|TTTGTCGTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTCAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAAT|
|000000122|SAMPLE-03|001|contig_1720|7111|142|G|571209d8eacfbec10|read-2|True|TTTGTCGTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAATAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAA|
|000000123|SAMPLE-03|001|contig_1720|7111|140|T|3dda82d075cb90188|read-2|False|TGTCGTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTTGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGG|
|000000124|SAMPLE-03|001|contig_1720|7111|140|G|4cc7969a78d30d313|read-2|False|TGTCGTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTA|
|000000125|SAMPLE-03|001|contig_1720|7111|140|G|418eca79d0630e0fe|read-2|False|TGTCGTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTATGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTC|
|000000126|SAMPLE-03|001|contig_1720|7111|140|G|6f72cff910f80d2c5|read-2|True|TGTCGTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTT|
|000000127|SAMPLE-03|001|contig_1720|7111|138|G|3fd470af01ec4eb4f|read-2|True|TCGTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTC|
|000000128|SAMPLE-03|001|contig_1720|7111|136|G|a533ced1530eea9a8|read-2|True|GTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCA|
|000000129|SAMPLE-03|001|contig_1720|7111|136|G|6a9f13baa13e23d0a|read-2|True|GTGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCA|
|000000130|SAMPLE-03|001|contig_1720|7111|135|G|72d19ae35f5136c1a|read-2|False|TGATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTA|
|000000131|SAMPLE-03|001|contig_1720|7111|134|G|529c1460d824e9bef|read-2|False|GATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTT|
|000000132|SAMPLE-03|001|contig_1720|7111|134|G|69c5dbf13623487fb|read-2|False|GATGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATTGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTCTATCTAA|
|000000133|SAMPLE-03|001|contig_1720|7111|132|G|fcd57363c61946297|read-2|False|TGATGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTG|
|000000134|SAMPLE-03|001|contig_1720|7111|129|G|c462177c026ee961e|read-2|True|TGATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAGTTA|
|000000135|SAMPLE-03|001|contig_1720|7111|128|G|2295d9de5ef4cf13e|read-2|False|GATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGGGTTATGG|
|000000136|SAMPLE-03|001|contig_1720|7111|127|G|305879fc8883daf8d|read-2|True|ATGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAAT|
|000000137|SAMPLE-03|001|contig_1720|7111|126|G|5df2a0285fcc03a9e|read-2|False|TGTTAGATGTCGCCTTAGGTTAAGCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTATGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGG|
|000000138|SAMPLE-03|001|contig_1720|7111|126|G|ee2961de43ccb9aa1|read-2|False|TGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCATGAG|
|000000139|SAMPLE-03|001|contig_1720|7111|126|G|3c7c5b2afc9694223|read-2|True|TGTTAGATGTCGCCTTAGGTTAATCTCTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAGTTATGGCT|
|000000140|SAMPLE-03|001|contig_1720|7111|126|G|0b0eb68568f992851|read-2|True|TGTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAACAACAATTTTATCTAATATGTCAGGAGTTATG|
|000000141|SAMPLE-03|001|contig_1720|7111|125|G|6ad74742e16c874d9|read-2|False|GTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAGTTATG|
|000000142|SAMPLE-03|001|contig_1720|7111|125|G|d8a10c29daa22874a|read-2|False|GTTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTA|
|000000143|SAMPLE-03|001|contig_1720|7111|124|G|2fcdca66158af9cc9|read-2|False|TTAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATC|
|000000144|SAMPLE-03|001|contig_1720|7111|123|G|eb182dc3869777d40|read-2|True|TAGATGTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAGTTA|
|000000145|SAMPLE-03|001|contig_1720|7111|118|G|07067ba83a92c090d|read-2|False|GTCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAG|
|000000146|SAMPLE-03|001|contig_1720|7111|117|G|221720449a9df5f2e|read-2|False|TCGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAGTTATGGCTTAT|
|000000147|SAMPLE-03|001|contig_1720|7111|116|G|6a32ac39d688c9342|read-2|True|CGCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAGTTAT|
|000000148|SAMPLE-03|001|contig_1720|7111|115|G|7a35d6e5df5c0313c|read-2|True|GCCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGATGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAGTTATGGCTTATAGTGGTA|
|000000149|SAMPLE-03|001|contig_1720|7111|114|G|d71843e1b8dfc97c1|read-2|False|CCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGATATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAGTTATGGCTTATAGTGGTAATAGTAATT|
|000000150|SAMPLE-03|001|contig_1720|7111|114|G|97810094800c2730d|read-2|False|CCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAGTTATGGCTT|
|000000151|SAMPLE-03|001|contig_1720|7111|114|G|a1a82ff1ac7d6c00a|read-2|True|CCTTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGTAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAGTTATGGCT|
|000000152|SAMPLE-03|001|contig_1720|7111|113|G|e79875a99e454d374|read-2|False|CTTAGGTTAATCTTTACATAATCGTAAGGACCGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAGTTATGGCTT|
|000000153|SAMPLE-03|001|contig_1720|7111|112|G|6b818ac19ef9992b2|read-2|False|TTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAGTTAT|
|000000154|SAMPLE-03|001|contig_1720|7111|112|G|33a1ab1044fbce5d2|read-2|True|TTAGGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAGTTATGGCT|
|000000155|SAMPLE-03|001|contig_1720|7111|109|G|ed19fd79f7f532930|read-2|False|GGTTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAGTTATGGCTTATAGTGGTAATAGTAAT|
|000000156|SAMPLE-03|001|contig_1720|7111|107|G|2eb280af5a55f65d2|read-2|False|TTAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAGTTATGGCTT|
|000000157|SAMPLE-03|001|contig_1720|7111|106|G|d6295261bd3682093|read-2|False|TAATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAGTTATGGCTTATAGTGGTAAT|
|000000158|SAMPLE-03|001|contig_1720|7111|106|G|e1324c70548d7aac2|read-2|False|TAATCTTTACATAATCTTAAGCAGAGTTGTATAGTTTCGTTTCTGTAGTTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAGTTATGGCTTATAGTGGTAAT|
|000000159|SAMPLE-03|001|contig_1720|7111|106|G|e0ec923db2ffe9978|read-2|True|TAATCTTTACATAATCTTAAGCACAGTTGTATAGCTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAGTTATGGCTTATAGTGGTAATAGTAATTTACCGGG|
|000000160|SAMPLE-03|001|contig_1720|7111|104|G|7cc251d99ddec1738|read-2|False|ATCTTTACATAATCTTAAGCACAGTTGTATAGTTTCGTTTCTGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAGTTATGGCTTATAGTGGTAATAGTAAT|
|000000161|SAMPLE-03|001|contig_1720|7111|100|G|18f3cf83405581ea6|read-2|False|TTACATAATCGTAAGCACAGTTGTATAGTTTCGTTTCAGTAATTAAGTAAAATGAGGTTAAAGAGGTGACAGAAATGAAAAAGAGATTAGGGTTAGGTTTGGGAATGTTTTTAATAACAATTTTATCTAATTTGTCAGGAGTTATGGCTTATAGTGGTAATAGTAATTTACCGGGAAGT|
|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|(...)|

Where

* `sample_id` matches to the input BAM file name,

* `request_id` matches to the order of the contig name in the input file,

* `pos_in_contig` marks the position of interest declared in the input file,

* and `pos_in_read` marks the actual location of the nucleotide in the short reads that corresponds to the position of interest.


{:.notice}
Edit [this file](https://github.com/merenlab/anvio/tree/master/anvio/docs/artifacts/linkmers-txt.md) to update this information.

