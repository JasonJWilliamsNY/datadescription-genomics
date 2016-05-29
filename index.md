---
layout: lesson
root: .
title: Intro to E.coli LTE Experiment
contributors: ["Jon Badalamenti","Amanda Charbonneau","Shari Ellis","Chris Fields","Bob Freeman","Chris Hamm","Randall Hayes","Josh Herr","Kate Hertweck","Adina Howe","Hilmar Lapp","Michael Linderman","Andréa Matsunaga","Blaine Marchant","Sue McClatchy","Sheldon McKay","Susan Miller","Jeramia Ory","Deborah Paul","Mary Shelley","Mike Smorul","Sara Stevens","Tracy Teal","Juan Ugalde","Jason Williams","Laura Williams","Ryan Williams", "Greg Wilson"]
minutes: 5
---



## Learning objectives for the entire set of Data Carpentry genomics lessons

Lessons introduce and reinforce basic skills in the Unix shell and R, and are **designed for learners with no programming experience.** The general topics and skills covered include:


### Interacting with Computers
- Could Computing
- Connecting to remote computing (SSH/PuTTY)
- File Transfer (FileZilla, other command-line tools: scp, rsynch, wget, etc. )

### Data Management and Organization
- Open source
- Metadata and reproducibility
- Important genomics file formats (CSV/TSV, FastQ, SAM/BAM, VCF, etc.)
- Organizing a filesystem for computational projects (Linux)
- Unix Shell (command-line: ls, cd, mkdir, cp, rm, wc, grep, cut, columns, head, tail, less etc,)
- R: Creating projects, scripts, and examining data

### Data Cleaning and visualization
- R: various packages and functions
- R: dplyr 
- R: ggplot
- FastQC - quality control of high-throughput sequence data
- Trimmomatic - filtering and trimming of high-throughput sequence data
- Integrated Genome Viewer

### Automation and scripting
- R scripting
- 'For' loops
- Building automated pipelines
- Using multithreaded applications

## Overview of our Data Set and Narrative

Microbes are ideal organisms for exploring 'Long-term Evolution Experiments' (LTEEs) - thousands of generations can be generated and stored in a way that would be virtually impossible for more complex eukaryotic systems. In [Lenski et.al.](http://www.nature.com/nature/journal/v489/n7417/full/nature11514.html), 12 populations of *Escherichia coli* were propagated for more than 40,000 generations in a glucose-limited minimal medium. This medium was supplemented with citrate which *E. coli* cannot metabolize in the aerobic conditions of the experiment. Sequencing of the populations at regular time points reveals that spontaneous citrate-using mutants (Cit+) appeared in a population of *E.coli* (designated Ara-3) at around 31,000 generations. It should be noted that spontaneous Cit+ mutants are extraordinarily rare - inability to metabolize citrate is one of the defining characters of the *E. coli* species. Eventually, Cit+ mutants became the dominate population as the experimental growth medium contained a high concentration of citrate relative to glucose. 

## Why we chose this data set
Data Carpentry workshops follow a narrative to illustrate key steps in the data analysis from the perspective of real experiment (and experimenter). We  choose the Lenski data for several reasons, including:

* Simple, but iconic NGS-problem: Examine a population where we want to characterize changes in sequence *a priori* 
* Dataset publicly available - in this case through the NCBI Sequence Read Archive (http://www.ncbi.nlm.nih.gov/sra)
* Small file sizes - while several of related files may still be hundreds of MBs, overall we will be able to get through more quickly then if we worked with a larger eukaryotic genome

**Purpose of these lessons**<br>
These lessons teach fundamental data management and analysis skills needed to work with genomic data. Example workflows are used to illustrate the researchers skills needed to handle files, use bioinformatics tools, and analyze their output.

**Teaching layout**<br>
Lessons are a series of modules designed for use at a two-day Data Carpentry workshop. They can also be covered by learners independently on their own - provided they follow the **Doing this on your own** setup requirements. Most lessons include work at the command line in the Unix shell (particularly the [Bash shell](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29)). We will also cover visualization of datasets in R and with some other common genome visualization tools. 

**Intended audience**<br>
We created for learners who are just starting to analyze a genomic dataset - which we define as any project that takes high-throughput (next-generation) sequence data to any number of endpoints (genome/transcriptome assembly, variant detection, RNA/ChIP-Seq, etc.). 



**Content Contributors: {{page.contributors | join: ', ' %}}**


<br>
####References
Blount, Z.D., Barrick, J.E., Davidson, C.J., Lenski, R.E. Genomic analysis of a key innovation in an experimental Escherichia coli population
(2012) Nature, 489 (7417), pp. 513-518.
