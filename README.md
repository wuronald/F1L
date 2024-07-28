# F1L
The repository contains projects associated with the Figure 1 Lab (F1L) initiative from Dean Lee. The goal of F1L is to develop compbio skills through reproduction of Figure 1 from scientific publications. 

## F1L Internship Emulator
Over the next 6 weeks, I will attempt to answer the following question posed by the inaugural F1L Internship Emulator:

> In this iteration of the F1L Internship Emulator, participants will play the role of a compbio intern in biotech/pharma. The intern is given this open-ended question: Using available scRNA-seq data from cancer cell lines, how would you explore the use of the following FDA-approved antibody therapies in other cancers?
> + Trastuzumab: Targets HER2 and is used in the treatment of HER2-positive breast and gastric cancers.
> + Bevacizumab: Targets VEGF and is used for a variety of cancers, including colorectal, lung, glioblastoma, breast, liver, and kidney cancer.

### Key Scientific Question (KSQ)
> Using available scRNA-seq data from cancer cell lines, how would you explore the use of the following FDA-approved antibody therapies in additional cancers?
Trastuzumab: Targets HER2 and is used in the treatment of HER2-positive breast and gastric cancers.
Bevacizumab: Targets VEGF and is used for a variety of cancers, including colorectal, lung, glioblastoma, breast, liver, and kidney cancer.

## Progress
1. Week 1: [Memo (Week 1)](##Memo (Week 1))
2. Week 2: [Memo (Week 2)](##Memo (Week 2))
3. Week 3:
4. Week 4:
5. Week 5:
6. Week 6
7. Week 7:
8. Week 8:

## Memo (Week 1)
The KSQ asks us to explore the potential utility of two FDA-approved molecularly targeting agents in other cancers that are currently not approved indications. Specifically, it asks us to use scRNA-seq data from cancer cell lines as a resource of explore this question. 

A key assumption behind the potential efficacy of these drugs is that the treated cancer cells expresses the target of these agents. In other words, a given cancer cell line may potentially be treated with Trastuzumab or Bevacizumab if they express the targets HER2 or VEGF, respectively. In addition, the cancer cells must also depend on these targets, such that they are sensitive to the loss of these targets. For example, HER2-positive breast cancers expresses very high levels of HER2 and have a dependency on HER2 activity for their survival and are sensitive to Trastuzumab. 

Cancer cell lines are the gold standard pre-clinical workhouse for cancer biologists. They are important models for the drug discovery pipeline. As such, there have been a tremendous effort in the community to characterize the sensitivity of anti-cancer agents and even existing FDA-approved drugs to large number of cancer cell lines. The [Cancer Cell line Encyclopedia and DepMap portal](https://depmap.org/portal/ccle/) are useful resources that can help us answer the KSQ. It is important to note that cancer cell lines are imperfect models of their respective cancers and *in silico* findings derived from these models may not necessarily translate to the clinic.

Lastly, we will be using scRNA-seq data from cancer cell lines to answer the KSQ. The ability of scRNA-seq to dissect the heterogeneity of cancer cell lines will be integral for identifying the expression of the targets of Trastuzumab or Bevacizumab. Additional functional studies with cancer cell lines coupled with scRNA-seq such as through Perturb-seq, a technique that utilizes CRISPR-based KO libraries coupled with a transcriptomic readout, may also be useful. Taken together, scRNA-seq data can potentially allow us to shortlist potential tumour-types for treatment with Trastuzumab and/or Bevacizumab.

## Memo (Week 2)
For week 2 we are tasked with reading the primary paper from [Kinker et al](https://www.nature.com/articles/s41588-020-00726-6). In this paper, the Tirosh lab conducts a monumental and expensive effort of scRNA-seq profiling on a large collection of cancer cell lines from a variety of cancer types (198 cancer cell lines; 22 cancer types; 53,513 total cells). 

> How did the authors handle the potential caveat of co-culturing cell lines before profiling by scRNA-seq? Why do you think that caveat was or was not adequately addressed?

> The authors identified discrete subpopulations of cells within a subset of individual cell lines (Fig. 2A-B). What might be the reason why some cell lines have these discrete subpopulations while others do not?

> What are Recurrent Heterogeneous Programs (RHPs) and how were they defined?

How do the identified RHPs relate to in vivo programs of heterogeneity in tumors, and what evidence supports this relationship?

> Where can you download the scRNA-seq data as shown in Figure 1B?
We can download the scRNA-seq data shown in Figure 1B from two sources mentioned in the **Data availability** section of the paper :

1. Broad Institute's Single Cell Portal: [SCP542](https://singlecell.broadinstitute.org/single_cell/study/SCP542/pan-cancer-cell-line-heterogeneity)
2. Gene Expression Omnibus (GEO): [GSE157220](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE157220)
    + Supplementary file: A large file (1.7 Gb) containing the counts-per-million (CPM) data across all cells.
        + Not sure how to use this file, seems atypical for scRNA-seq. Perhaps this is the counts matrix?
    + Additional links for each sample to the raw bam files stored on the SRA is also included.
