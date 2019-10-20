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

<!-- Picture so Male/Female Fly and Ovary/Testis -->

<!-- Genome summary highlighting -->

---

# Testis Biased Gene Expression

<!-- DEG picture of Whole Body (M vs F) -->
<!-- DEG picture of Whole Body (M vs F) no gonad -->

---

# Objectives

Use available RNA-Seq data to generate *D. melanogaster* testis specific transcriptome assembly.

Use PacBio data for validation of novel transcripts.

---

layout: true

.header[

- RNA-Seq Assembly

]

---

# Sequence Read Archive (SRA)

<!-- Overview of SRA -->

---

# Re-processing Workflow

<!-- Pre-alignment and alignment workflows -->

---

# Metadata Workflow

<!-- Metadata processing -->

---

# Testis RNA-Seq

<!-- Summary of testis RNA-Seq data -->

---

# Testis Assembly

<!-- Stringtie assembly info -->

---

layout: true

.header[

- PacBio Validation

]

---

# PacBio Samples

<!-- PacBio Experimental Design -->

---

# Iso-Seq Workflow

<!-- Workflow enough details to get feedback -->

---

# Adult Validation


---

# Larval Validation

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
