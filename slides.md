---
theme: ./theme
colorSchema: bright
layout: intro
highlighter: shiki
lineNumbers: false
title: Analyzing genomics data
info: |
  ## Omics Data Analysis: Genomics
  How to obtain biological information from the measurements.
drawings:
  persist: false
css: unocss
themeConfig:
  primary: '#5d8392'
  logoHeader: /assets/scilifelab.png
  eventLogo: >-
    /assets/ngilogo.png
  eventUrl: https://ngisweden.scilifelab.se/
---

# Analyzing genomic data

From data to insight (hopefully)

---
layout: presenter
presenterImage: '/assets/people/matthias.jpg'
---

# Matthias Zepper

- Life and Medical Sciences in Bonn 🇩🇪
- PhD in leukemia epigenetics in Münster 🇩🇪
- Founder (& liquidator) of start-up [Nucleotidy](http://nucleotidy.bio)
  <div class="rounded-md overflow-hidden" w="40%" style="background-color: #073a4d; padding: 1em">
  <img src="https://raw.githubusercontent.com/nucleotidy/nucleotidy-landing/main/src/assets/images/logos/nucleotidyweblogo.svg" alt="Nucleotidy logo" />
  </div>
- Bioinformatician at the NGI, Stockholm 🇸🇪

---
layout: center
---
<div class="rounded-md overflow-hidden vidcontent" w="100%"><span>An exciting day in the lab...</span>
  <video preload="auto"  controls class="w-full -m-1px border-none outline-none p-0" src="/assets/phdcomics/research.mp4" type="video/mp4"></video>
</div>

---
layout: text-image
media: '/assets/fun/phd021315s.gif'
caption: 'https://phdcomics.com/comics/archive.php?comicid=1780'
---

# Bioinformatician

## The toolbox

## Genomic data formats

## Exemplary analyses

## Workflows

---
layout: intro
---

# Toolbox peek

---
layout: text-image
reverse: true
media: '/assets/tools/excel/nameerrors.png'
caption: 'https://doi.org/10.1186/s13059-016-1044-7'
---

# Use suitable tools

<a href="https://www.nature.com/articles/s41588-020-0669-3">
<img src="/assets/tools/excel/renamedgenes.png" alt="Gene renaming by HGNC." />
</a>

In 2020, _Human Genome Gene Nomenclature Committee (HGNC)_ renamed genes that were auto-converted to dates in Excel.

---
layout: text-image
media: '/assets/tools/excel/conversionoptional.png'
caption: 'https://gizmodo.com/microsoft-fixes-excel-feature-that-forced-scientists-to-1850949443'
---

# Use suitable tools


<div class="mx-auto my-auto">
  <img src="/assets/fun/excel.png" class="rounded-full w-80 mx-auto"/>
</div>

---
layout: text-window
---

# Use suitable tools

- They might not have a GUI.
- They might not run on your machine.
- For remote compute, mind data privacy!

# Use a suitable OS

- GNU / Linux
- MacOS
- Windows Subsystem for Linux

::window::

```
_   _ ____  ____  __  __    _    __  __
| | | |  _ \|  _ \|  \/  |  / \   \ \/ /   | System:    rackham3
| | | | |_) | |_) | |\/| | / _ \   \  /    | User:      bioinfomagician
| |_| |  __/|  __/| |  | |/ ___ \  /  \    |
 \___/|_|   |_|   |_|  |_/_/   \_\/_/\_\   |

########################################################################

  User Guides: http://www.uppmax.uu.se/support/user-guides
  FAQ: http://www.uppmax.uu.se/support/faq

  Write to support@uppmax.uu.se, if you have questions or comments.


(base) [bioinfomagician@rackham3 ~]$




```

---
layout: new-section
---

# Programming languages for data exploration

<div class="grid grid-cols-3 gap-1 py-4">

<div class="mx-auto">
  <img src="https://upload.wikimedia.org/wikipedia/commons/1/1f/Python_logo_01.svg" class="rounded-full w-50 mx-auto"/>
</div>
<div class="mx-auto">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/1b/R_logo.svg/620px-R_logo.svg.png" class="rounded-full w-50 mx-auto"/>
</div>
<div class="mx-auto">
  <img src="https://upload.wikimedia.org/wikipedia/commons/1/1f/Julia_Programming_Language_Logo.svg" class="rounded-full w-50 mx-auto"/>
</div>

<div>
  <p class="text-lg text-gray-500 font-semibold text-center">Python</p>
</div>
<div>
  <p class="text-lg text-gray-500 font-semibold text-center">R</p>
</div>
<div>
  <p class="text-lg text-gray-500 font-semibold text-center">Julia</p>
</div>
</div>


---
layout: new-section
---

# Programming languages for tools

<div class="grid grid-cols-3 gap-1 py-4">

<div class="mx-auto">
   <img src="https://upload.wikimedia.org/wikipedia/commons/1/18/ISO_C%2B%2B_Logo.svg" class="rounded-full w-50 mx-auto"/>
</div>
<div class="mx-auto my-auto">
  <img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Go_Logo_Blue.svg" class="rounded-full w-50 mx-auto"/>
</div>
<div class="mx-auto">
  <img src="https://upload.wikimedia.org/wikipedia/commons/d/d5/Rust_programming_language_black_logo.svg" class="rounded-full w-50 mx-auto"/>
</div>

<div>
  <p class="text-lg text-gray-500 font-semibold text-center">C++</p>
</div>
<div>
  <p class="text-lg text-gray-500 font-semibold text-center">Go</p>
</div>
<div>
  <p class="text-lg text-gray-500 font-semibold text-center">Rust</p>
</div>
</div>

---
layout: new-section
---

# Bioinformatic ecosystem

<div class="grid grid-cols-4 grid-rows-2 grid-flow-row-dense">

<div class="mx-auto my-auto">
  <img src="https://upload.wikimedia.org/wikipedia/commons/e/e0/Git-logo.svg" class="rounded-full w-30 mx-auto"/>
   <p class="text-lg text-gray-500 font-semibold text-center">git (version control)</p>
</div>
<div class="mx-auto my-auto">
   <img src="https://upload.wikimedia.org/wikipedia/commons/3/38/Jupyter_logo.svg" class="rounded-full w-30 mx-auto"/>
   <p class="text-lg text-gray-500 font-semibold text-center">Jupyter, Quarto (Notebooks)</p>
</div>
<div class="mx-auto my-auto">
   <img src="https://upload.wikimedia.org/wikipedia/commons/c/c7/Snakemake_logo_dark.png" class="rounded-full w-30 mx-auto"/>
   <img src="https://raw.githubusercontent.com/seqeralabs/logos/master/nextflow/nextflow_logo_color.svg" class="rounded-full w-30 mx-auto"/>
   <p class="text-lg text-gray-500 font-semibold text-center">Snakemake, Nextflow (Workflows)</p>
</div>
<div class="mx-auto my-auto">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a7/Docker-svgrepo-com.svg/480px-Docker-svgrepo-com.svg.png" class="rounded-full w-30 mx-auto"/>
   <p class="text-lg text-gray-500 font-semibold text-center">Docker, Apptainer (containers)</p>
</div>

<div class="mx-auto my-auto">
   <img src="https://bioconda.github.io/_images/bioconda.png" class="rounded-full w-30 mx-auto"/>
   <p class="text-lg text-gray-500 font-semibold text-center">Bioconda (package manager)</p>
</div>

<div class="mx-auto my-auto">
  <img src="https://upload.wikimedia.org/wikipedia/commons/e/e4/Bioconductor_logo_rgb.jpg" class="rounded-full w-30 mx-auto"/>
   <p class="text-lg text-gray-500 font-semibold text-center">Bioconductor, Tidyverse (R packages)</p>
</div>
<div class="mx-auto my-auto col-span-2">
   <img src="https://arrow.apache.org/img/arrow.png" class="rounded-full w-30 mx-auto"/>
   <p class="text-lg text-gray-500 font-semibold text-center">BioNumPy, Pandas, Polar.rs, Apache Arrow, DuckDB (Analytics)</p>
</div>

</div>

---
layout: new-section
---

# The most important tools

<div class="grid grid-cols-2 gap-1 py-4">

<div class="mx-auto">
  <img src="/assets/tools/books/alberts.jpg" class="rounded-full w-50 mx-auto"/>
</div>
<div class="mx-auto">
  <img src="/assets/tools/books/hastie.png" class="rounded-full w-50 mx-auto"/>
</div>

<div>
  <p class="text-lg text-gray-500 font-semibold text-center">Biological understanding</p>
</div>
<div>
  <p class="text-lg text-gray-500 font-semibold text-center">Statistical knowledge</p>
  <a href="https://hastie.su.domains/ElemStatLearn/printings/ESLII_print12.pdf">(free fulltext)</a>
</div>
</div>


---
layout: new-section
---

# Syntax errors are easy to debug

<div class="mx-auto">
  <img src="/assets/tools/issues/syntaxerror.png" class="rounded-full w-200"/>
</div>


# but it frequently happens that 
# tools output _something_ arbitrarily.

---
layout: text-image
media: '/assets/tools/issues/PIIS1934590923002886.png'
caption: 'https://doi.org/10.1016/j.stem.2023.08.005'
---

# Understand the methods you apply

Example from [j.stem.2023.08.005](https://doi.org/10.1016/j.stem.2023.08.005):

- Findings backed by wet lab results.
- Distances in 2D projections of UMAP / t-SNE are not directly interpretable.
- Their loss functions are invariant with respect to rotations.
- More details at [Understanding UMAP](https://pair-code.github.io/understanding-umap/)


---
layout: text-image
media: '/assets/tools/issues/s41586-020-2095-1.png'
---

# Understand the methods you apply

Example from [10.1038/s41586-020-2095-1](https://www.nature.com/articles/s41586-020-2095-1):

- In this case, both the analysis strategy and the understanding of the used methods was inadequate.
- Overconfident broad generalization of the findings.
- More details at [10.1128/mbio.01607-23](https://journals.asm.org/doi/10.1128/mbio.01607-23)

---
layout: intro
---

# Common genomic data formats


---
layout: new-section
---

# FastQ: Format for sequencing reads

<div class="grid grid-cols-4 gap-1 py-4">

<div class="mx-auto my-auto">
  <img src="/assets/bio/dnabackbone2.png" class="rounded-full w-20 mx-auto"/>
</div>
<div class="mx-auto">
  <img src="https://bioicons.com/icons/cc-by-4.0/Lab_apparatus/DBCLS/genome-sequencer-8.svg" class="rounded-full w-50 mx-auto" alt="genome-sequencer-8 icon by DBCLS https://togotv.dbcls.jp/en/pics.html is licensed under CC-BY 4.0 Unported https://creativecommons.org/licenses/by/4.0/"/>
  <img src="https://bioicons.com/icons/cc-by-4.0/Lab_apparatus/DBCLS/DNA_sequencer.svg" class="rounded-full w-35 mx-auto" alt="DNA_sequencer icon by DBCLS https://togotv.dbcls.jp/en/pics.html is licensed under CC-BY 4.0 Unported https://creativecommons.org/licenses/by/4.0/"/>
  <img src="https://bioicons.com/icons/cc-0/Genetics/PacBio/img_sequencers01.svg" class="rounded-full w-40 mx-auto" alt="img_sequencers01 icon by PacBio https://pacb.com is licensed under CC0 https://creativecommons.org/publicdomain/zero/1.0/"/>
</div>

<div class="mx-auto col-span-2">
  <img src="https://bioicons.com/icons/cc-0/General_items/OpenClipart/Document.svg" class="rounded-full w-40 mx-auto" alt="Document icon by OpenClipart https://openclipart.org/ is licensed under CC0 https://creativecommons.org/publicdomain/zero/1.0/"/>
  <p class="text-lg text-gray-500 font-semibold text-center">FastQ</p>
</div>
</div>

---
layout: new-section
---

# FastQ: Format for sequencing reads

<div class="w-160 m-auto" style="justify-content: left; text-align: left;">

- Plain text format
- Each read is represented by for consecutive lines:
  1. Sequence identifier and an optional description
  2. The sequence
  3. &#43; (optional) 
  4. The base call quality

```
@SCILIFELAB:500:NGISTLM:1:1101:32832:1016 1:N:0:GCTTCAGGGT+AAGGTAGCGT
TCCCCCAACTTGATATTAATAACACTATAGACCACCGCCCCGAAGGGGACGAAAAATGGTTTTTAGAGAACGAGAAGACGGTTACGCAG
+
F#FFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF:FFFFFFFFFFFFF
```

</div>

---
layout: two-cols-header
---

# Quality control

::left::

# Left

This shows on the left

::right::

# Right

This shows on the right
