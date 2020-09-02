
# FAIRbioinfo for bioinformaticians

## Introduction to the tools of reproducibility in bioinformatics

C. Hernandez<sup>1</sup>, T. Denecker<sup>1</sup>, J. Sellier<sup>2</sup> G., Le Corguille<sup>2</sup>, C. Toffano-Nioche<sup>1</sup>
<sup>1</sup> Institute for Integrative Biology of the Cell (I2BC) UMR 9198, Universit ́e Paris-Sud, CNRS, CEA 91190 - Gif-sur-Yvette, France
<sup>2</sup> IFB Core Cluster taskforce
_Sept. 2020_

## Literate programming

### Introduction

#### What is literate programming?

Let us change our traditional attitude to the construction of programs:
Instead of imagining that our main task is to instruct a computer what to do, let us concentrate rather on explaining to humans what we want the computer to do.

— Donald E. Knuth, Literate Programming, 1984

### Definition

”Literate programming is a programming paradigm introduced by Donald Knuth in which a computer program is given an explanation of its logic in a natural language, such as English, interspersed with snippets of macros and traditional source code, from which compilable source code can be generated.” 
Donald Knuth, 1984.

[Wikipedia](https://en.wikipedia.org/wiki/Literate_programming#Workflow)

### What does it look like?

![](https://i.imgur.com/xFBJotW.png)

Interactive programming interface allowing to combine both natural and computer languages.

In one file:

- Explanations
- Code
- Results
- Graphs and plots

### Why using literate programming frameworks?

Use cases:

- Day to day analyses
- Analysis reports
- Writing scientific articles

### Example of an article entirely written using a notebook

![](https://i.imgur.com/mgE0CxW.png)

## Markup and markdown

### Definition :

A markup language uses tags to define elements within a document.

### Three different types and usage :

- Presentational (used by traditional word-processing systems)
    - _Markup is invisible_
- Procedural, provides instructions to process the text (e.g. TeX,PostScript)
    - _Markup is visible and can be directly manipulated by the author._
- Descriptive, to label documents parts (e.g. LaTeX, HTML, XML...)
    - _Emphasizes the document structure._

### Markdown language

Markdown is a Lightweight markup language.  
Designed to be :

- easy to write using any generic text editor (plain-text-formatting syntax)
- easy to read in its raw form

### You’ve probably see it already on GitHub (README), Wikipedia...

![](https://i.imgur.com/3jZmdoz.png)

[Github guide](urlhttps://guides.github.com/features/mastering-markdown/)

### But how is this useful for literate programming?

When you want to weave both code (to be interpreted) and formatting information, you precisely need a lightweight language for the formatting part.

### The challengers

No need to hide, there are currently two main frameworks used in bioinformatics:
RMarkdown and Jupyter

## RMarkdown

At the beginning, there was nothing.

Then came Sweave.
Leisch, Friedrich (2002). ”Sweave, Part I: Mixing R and LaTeX: A short introduction to the Sweave file format and corresponding R functions”
And people saw that the path would be long...

### knitR (2011)

![](https://i.imgur.com/CFC3rZy.png)

”The knitr package was designed to be a transparent engine for dynamic report generation with R, solve some long-standing problems in Sweave,and combine features in other add-on packages into one package”

https://yihui.org/knitr/

![](https://i.imgur.com/zkpggVz.png)

”When you run render, R Markdown feeds the .Rmd file to knitr, which executes all of the code chunks and creates a new markdown (.md) document which includes the code and its output> The markdown file generated by knitr is then processed by pandoc which is responsible for creating the finished format.”
https://rmarkdown.rstudio.com

![](https://i.imgur.com/JX4qOak.png)

Integrated into RStudio, IDE for R.

### R Notebooks

![](https://i.imgur.com/UrC8Ixk.png)

### and more...

![](https://i.imgur.com/phE6qmh.png)

## Jupyter

### A bit of history...

- 2011 : IPython (interactive Python shell) with notebook functionalities
- 2014 : Spin-off project called Project Jupyter 
- a non-profit, open-source project maintained by a strong Community
- ”Jupyter will always be 100% open-source software, free for all to use and released under the liberal terms of the modified BSD license”
- A reference to the three core programming languages supported by Jupyter (Julia, Python and R)

https://jupyter.org/

What can it do?  
Everything (excepted coffee)

But what is it exactly?  
Web-based interactive computational environment.

- Web-based : client/server
- Interactive : notebook system
- Computational environment : console, many kernels available...

Dashboard
![](https://i.imgur.com/Bvb4rAy.png)

Notebook editor
![](https://i.imgur.com/1eDK1JE.png)

### Project Jupyter

- A non-profit, open-source project maintained by a strong Community
- Adopted by the biggest in the Cloud industry (Google, Microsoft, Amazon...)
- And financed by the biggest (Google, Microsoft, EU Horizon 2020 program, Alfred P. Sloan Foundation...)

Inside the Python community (snakemake, conda...)

Integration with GitHub since 2015 (renderer)

Nbviewer : a static renderer for Jupyter notebooks
![](https://i.imgur.com/zWCpnKC.png)
https://nbviewer.jupyter.org/

Jupyter + Docker = binder
![](https://i.imgur.com/j1do48D.png)
https://mybinder.org/

More to come : Jupyter Lab 1.0
![](https://i.imgur.com/I4ZRsRy.png)

## Conclusion ?

### Who’s the best?

It depends...
- R analyses? Go for RMarkdown/RStudio
- R analyses for a publication? Consider Jupyter with an R kernel
- Python analyses? Why do you even ask...

## Practical session

### Analysis workflow
![](https://i.imgur.com/3GWTvKj.png)
green=input, blue=tool

- fastqc control quality of the input reads
- bowtie2 reads mapping on the genome sequence
- samtools mapped reads selection & formatting
- HTseq count table of mapped reads on genes (annotations)
- DESeq2 statistical analysis: genes list having differential expression

## Practical session

### Savoir FAIRe

- Markdown
- Learn the structure of an Rmd file
- Turn a script into a notebook
- Extend the notebook with new functionalities
- Bonus: introduction to Jupyter