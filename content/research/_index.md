---
title: Research

# View.
#   1 = List
#   2 = Compact
#   3 = Card
#   4 = Citation
view: 4

# Optional header image (relative to `static/img/` folder).
header:
  caption: ""
  image: ""
---
My research focuses on the genetics of adaptation. I aim to understand how epistasis, pleiotropy, and the distribution of beneficial fitness effects (DBFE) affect the properties of adaptive walks, both experimentally, through the study of the relationships between genotype, phenotype, and fitness in microvirid bacteriophages (relatives of ΦX174), and computationally, through the development of methods of population genetic inference in organisms with skewed offspring distributions. During my graduate and postdoctoral work I have engaged in several projects aimed at understanding the forces shaping fitness landscapes and adaptive processes:

(1) Experimental measurement of pairwise epistasis in beneficial mutations:

Through the mutagenic construction of bacteriophage genotypes containing all possible pairs of three sets of five beneficial mutations that were originally identified during adaptation to: (i) simple growth; (ii) heat-shock; and (iii) pH-shock conditions, we found extensive support for the hypothesis that mutations interact additively with regard to their effect on phenotype, with epistasis for fitness effects resulting from a non-linear relationship between phenotype and fitness and pleiotropy between phenotypes.

{{< figure library="true" src="heatshock.jpg" title="" lightbox="true" >}}

In the figure above, we see significant and ubiquitous negative epistasis for pairs of beneficial mutations when looking at the level of fitness and growth rate, but on average mutations interacted additively when looking at their effects on a simple biophysical phenotype (Sackman AM, Rokyta DR. 2018. Additive phenotypes underlie epistasis of fitness effects. Genetics 208: 339-348. pdf). The next step in this research is to decompose the effects of beneficial mutations on the composite phenotype of growth rate into its constituent, simpler phenotypes (i.e., attachment rate, burst size, lysis time) to determine whether this pattern holds for all phenotypes. This work would provide experience for undergraduates in genetic techniques including mutagenesis, PCR, and Sanger sequence analysis as well as basic phage and cell culturing.

(2) Estimation of the DBFE and the rate of parallel evolution:

The shape of the beneficial tail of the overall distribution of mutational fitness effects forms a basic assumption at the heart of all models of adaptation. Historically, it has generally been assumed that the DBFE takes the form of the exponential distribution, but recent work in experimental evolution has found evidence for heavy-tailed or truncated distributions. The shape of the DBFE determines many properties of adaptation, including the rate of adaptation, the average step size in an adaptive walk, and the rate of parallel evolution.  A thorough characterization of the DBFE, which has rarely been performed experimentally, is therefore critical to our basic understanding of adaptive processes. As part of my graduate work, I characterized the DBFE through 20 replicate first steps of adaptation for four divergent wild phage genotypes. We found that all four genotypes were best described as having truncated distributions.  Below, we show that although parallel evolution was frequent both within and across genotypes, parallel evolution was being driven at least as much by mutational biases as by selection, with suboptimal beneficial mutations fixing repeatedly in replicates of all four genotypes (Sackman AM, McGee LW, Morrison AJ, Pierce J, Anisman J, Hamilton H, Sanderbeck S, Newman C, Rokyta DR. 2017. Mutation-driven parallel evolution during viral adaptation. Molecular Biology and Evolution 34: 3243–3253. pdf).

{{< figure library="true" src="parallel.jpg" title="" lightbox="true" >}}

It has been hypothesized that the shape of the DBFE may change as populations move toward an optimum, and as part of my future work I propose to investigate changes in the DBFE through densely time-sampled population genomic sequencing of viral populations across an entire adaptive walk, starting from an unadapted, low-fitness genotype to a fully adapted genotype at a peak in its adaptive landscape.  I predict that the DBFE should become less exponential or heavy-tailed as the population converges on an optimum and mutations of large effect become more rare. This type of project would present the opportunity for engaging undergraduate researchers both in the basics of experimental viral evolution and in the preparation and analysis of high-throughput sequence data, and would also be a good application for the population genetic inference software described below.

(3) Direct measurement of pleiotropy and the cost of complexity

A direct prediction of Fisher’s geometric model is that the rate of adaptation decreases as organisms become more complex, or as the number of phenotypes under selection increases. This purported “cost of complexity” arises from antagonistic pleiotropy between traits. In viruses, it is hypothesized that antagonistic pleiotropy arises between the traits of viral growth rate and capsid stability, as there is a relatively narrow range of optimal binding affinities between capsid subunits that allow for proper assembly of the capsid. We tested these predictions by performing complete adaptive walks of both wild and growth-adapted phage strains under complex selection acting on both growth rate and stability. Most surprisingly (shown in the figure below from Sackman and Rokyta, in revision, Genetics, pdf), both wild-type strains were able to increase growth rate and stability at the same time, and growth-adapted strains significantly increased stability with no cost to growth rate. Additionally, the rate of adaptation was actually higher under complex selection relative to simple selection. Our results imply that human pathogens may be able to adapt to novel hosts or environments more quickly than anticipated under models that assume widespread antagonistic pleiotropy, and without incurring tradeoffs for growth in their original environments.

{{< figure library="true" src="longterms.jpg" title="" lightbox="true" >}}


(4) Inference of population genetic parameters under sweepstakes reproduction

With the development and improvement of high-throughput sequencing technology, there has been a great increase in the availability of time-sampled population genomic data, particularly in experimentally evolved populations. However, the biology of many organisms, such as certain groups of marine organisms, plants, and viruses characterized by highly variable offspring distributions, or so-called “sweepstakes reproduction”, makes the application of standard methods of population genetic inference—based on the Wright-Fisher (WF) model and Kingman’s coalescent—highly problematic.

Several classes of multiple merger coalescent (MMC) models have been created to account for violations of the assumptions of the Kingman that result from skewed offspring distributions. Of particular interest is the Ψ-coalescent, under which the parameter Ψ describes the proportion of the population in one generation that are the descendants of a single parent in the previous generation. In the figure below (Sackman, Harris, and Jensen. 2019. Inferring demography and selection in organisms characterized by skewed offspring distributions. In press, Genetics, 10.1534/genetics.118.301684), we show the effect of sweepstakes reproduction on the site-frequency spectrum and Tajima’s D.

{{< figure library="true" src="sfstaj.jpg" title="" lightbox="true" >}}

We have created a new methodology, MMC-ABC (available here [add link]), which jointly estimates a genome-wide value of Ψ alongside site-specific selection coefficients from time-series polymorphism data, with the goal of applying MMC-ABC to data from experimentally evolved viral populations. Below, we compare the ability of MMC-ABC to accurately estimate selection coefficients (s) under strong offspring skew (left) with estimation of s under a WF model (right). Continued development and application of methods for population genetic inference that are better suited to the biology of viruses will be highly applicable to the time-series population genomic data generated by my research and will provide student researchers with opportunities for experience in biological modeling and bioinformatic analysis.

{{< figure library="true" src="corr.jpg" title="" lightbox="true" >}}
