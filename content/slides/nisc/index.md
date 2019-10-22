---
title: "NISC Talk"
url: "/slides/nisc/"
image: "/slides/nisc/cover.jpg"
description: "NISC performed all of our recent PacBio sequencing. They asked me to come and talk about how we are using this data."
ratio: "16:9"
themes:
- apron
- adirondack
- descartes
---
class: title
background-image: url(cover.jpg)

# Re-annotating the Drosophila Testis' Transcriptome

.footer[
-  October 23, 2019
-  @NISC
]

---

# .center[Justin M. Fear]

.header[
- About
]

.fl.db.w-50pct[
- IRTA Fellow (NIDDK/NIH)
    - <i class="fas fa-dna"></i> Genomics
    - <i class="fas fa-project-diagram"></i> Gene Regulation
    - <img src="https://www.pngfind.com/pngs/m/594-5940907_file-icon-drosophila-melanogaster-svg-drosophila-cartoon-hd.png" width="6%" /> Drosophilist

]

.fr.db.w-50pct[
- Contact:
    - <i class="fab fa-github"></i>jfear
    - <i class="fas fa-envelope-open-text"></i> justin.fear@nih.gov
    - <img src="https://avatars1.githubusercontent.com/u/13694414?s=400&u=056f5db90f080c2072519de480b976bc46521633&v=4" width="6%"/> geneticsunderground.com
]

--

<hr>

### Project Code

.fl.db.w-50pct[
**SRA**

<i class="fab fa-github"></i>jfear/ncbi_remap
]
.fr.db.w-50pct[

**PacBio**

<i class="fab fa-github"></i>jfear/dmel_pacbio

<i class="fab fa-github"></i>jfear/dmel_larval_pacbio
]

---
layout: true

.header[
- Introduction
]

---

# *Drosophila melanogaster*

<!-- Adults -->
![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ5oqRRU4VBMcihHWePJ4ngAJYD7JasuAsw3Ydc-pdPxNMBw8sh# w-6-12th db absolute l-0 t-4)
![](https://www.genetics.org/content/genetics/208/3/875/F4.large.jpg# w-2-12th db absolute l-2 b-2)
![](https://www.g3journal.org/content/ggg/7/9/3145/F1.large.jpg# w-2-12th db absolute l-3-12th b-2)

<!-- larva -->
![](https://www.barnardhealth.us/drosophila-melanogaster/images/2057_109_50-drosophila-larvae-slide.jpg# w-40pct db absolute r-2 t-2)
![](/sra_presentations/images/larval_testis.png# w-40pct db absolute b-1 r-2)

---

# Drosophila genome

![](/sra_presentations/images/drosophila_genome.png# w-70pct center db absolute t-2-12th)

![](/sra_presentations/images/drosophila_genome_track.png# w-70pct center db absolute b-0)

---

# Testis-biased Gene Expression

.fl.db.w-40pct[
Most differences between males and females are due to testis-biased expression.

The testis uniquely expresses a large number of transcripts that are required for spermatogenesis.
]

![](/sra_presentations/images/testis_biased_expression.png# db w-50pct fr)

.footer[
- Parisi et al. 2003. *Science*
]
---

# .dn[Objectives]

.w-90pct.absolute.t-3.pa-3.ba.br-5.bg-darkred.color-white[
## Problem:

Testis transcripts are under-represented in current annotations.
]

.w-90pct.absolute.b-2.pa-3.ba.br-4.bg-darkgreen.color-white[
## Objectives:

1. Transcriptome assembly using publicly available testis-specific RNA-Seq data.

2. Transcriptome assembly using testis-specific PacBio data.

]

---

layout: true

.header[

- RNA-Seq Assembly

]

---

# Drosophila Sequence Read Archive

![](/sra_presentations/images/insdc.svg# w-60pct fl)

--

.fs-150.fr[
| Strategy      | Count  |
| ------------- | ------ |
| RNA-Seq       | 20,420 |
| DNA-Seq       | 8,007  |
| ChIP-Seq      | 5,898  |
| Other         | 21,629 |
| **Completed** | 43,692 |
]

---

# SraMongo

![](/sra_presentations/images/sramongo_website.png)

---

# .dn[Re-processing Workflow]

![](/sra_presentations/images/aln_workflow.svg)

---

# Alignment Workflow cont.

![](/sra_presentations/images/mapping.svg)

---

# .dn[GEO Submission]

![](/sra_presentations/images/geo_submission.png# w-7-12th absolute t-0 center)

---

# .dn[Metadata Workflow]

![](/sra_presentations/images/downstream_biometa.svg)

---

# Testis RNA-Seq (109 samples)

![](/sra_presentations/images/testis_corr.svg# w-50pct absolute l-0 b-0)
![](/sra_presentations/images/testis_pca.svg# w-50pct absolute r-0 b-2)

---

# StringTie

.w-30pct.db[Testis RNA-Seq data is used to assembly testis-specific transcriptome.]

![](/sra_presentations/images/stringtie.png# w-70pct absolute t-0 r-0)

.footer[
- Pertea et al. 2015. *Nature Biotechnology*
]

---

# Testis Assembly (SRA + StringTie)

.db.absolute.t-10pct.l-1[
![](/sra_presentations/images/merged_genes.png)
![](/sra_presentations/images/huge_introns.png)
]

.absolute.b-1.l-5-12th[
| category      | count  |
| ------------- | ------ |
| Novel Exons   | 44,155 |
| Novel Introns | 26,307 |
| Novel Loci    | 12,129 |
]

---
layout: true

.header[
- PacBio Validation
]

---

# PacBio Samples

.db.absolute.l-3-12th[
| sample            | machine      | # HQ Polished |
| ----------------- | ------------ | ------------- |
| Adult male        | PacBio RS II | 12,565        |
| Adult testis R1   | PacBio RS II | 12,448        |
| Adult testis R2   | Sequel II    | ---           |
| Larval testis TR1 | Sequel       | 83,066        |
| Larval testis TR2 | Sequel II    | ---           |
]

![](https://www.g3journal.org/content/ggg/7/9/3145/F1.large.jpg# w-20pct db absolute l-4 b-1)
![](/sra_presentations/images/larval_testis.png# w-50pct db absolute b-1 r-1)

---

# Iso-Seq Workflow

<!-- Workflow enough details to get feedback -->

---

# Adult Validation

![](/sra_presentations/images/adult_testis_sqanti.png# w-7 absolute b-0 r-0)

.w-40pct[
PacBio (RS II) adult testis samples captured ~8k isoforms.
]

| category      | count  |
| ------------- | ------ |
| Novel Exons   | 225 |
| Novel Introns | 236 |
| Novel Loci    | 43 |

---

# .fs-90[Larval Validation]

![](/sra_presentations/images/larval_testis_sqanti.png# w-7 absolute b-0 r-0)

.w-4-12th[
PacBio (Sequel) larval testis samples captured ~36k isoforms.
]

| category      | count  |
| ------------- | ------ |
| Novel Exons   | 2,840 |
| Novel Introns | 2,242 |
| Novel Loci    | 707 |

---

# .dn[Visualization]

---
layout: true

.header[
- justin.fear@nih.gov
- geneticsunderground.com
- github.com/jfear
]

.footer[
- <sup>*</sup>Former Lab Members
]

---
class: compact

# Acknowledgements

.fl.db.fs-80.mr-4[
## Oliver Lab

- Brian Oliver
- Zhen-Xia Chen<sup>*</sup>
- Isabelle Berger<sup>*</sup>
- Sharvani Mahadevaraju
- Leif Benner
- Kathryn McClelland
- Pradeep Bhaskar
]

.fl.db.fs-80.mr-4[
## SRA/GEO

- Tanya Barrett (GEO)
- Emily Clough (GEO)<sup>*</sup>
- Christopher O'Sullivan (SRA)
- Ben Busby (NLM)
- Jean Thierry-Mieg (NLM)
- Danielle Thierry-Mieg (NLM)
]

.fl.db.fs-80.mr-5[
## NISC

- Alice Young
- Morgan Park
- Gerry Bouffard
]

.fl.db.fs-80[
## FlyBase

- Norbert Perrimon
- Gil dos Santos
- Christopher Tabone
- Lynn Crosby
- Beverly Matthews
- Julie Agapite
- Claire Hu
- Susan Russo
]
