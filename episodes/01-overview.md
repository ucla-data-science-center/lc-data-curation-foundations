---
title: "Overview of Scientific Reproducibility"
teaching: 30
exercises: 15
questions:
- "How is 'reproducibility' defined?"
- "Why is scientific reproducibility important?"
objectives:
- "Differentiate among various definitions of 'reproducibility' and other related concepts."
- "Recall historical and contemporary imperatives for scientific reproducibility."
keypoints:
- "The term 'reproducibility' has been used in different ways in different disciplinary contexts."
- "Computational reproducibility, which is the focus of this and follow-up lessons, refers to the duplication of reported findings by re-executing the analysis with the data and code used by the original author to generate their findings."
- "Scientific reproducibility is not a novel concept, but one that has been reiterated by prominent scholars throughout history as a cornerstone of scientific practice."
- "Failed attempts to reproduce published scientific research are considered by some to be reflective of an ongoing crisis in scientific integrity."
- "Stakeholders have taken note of the importance of reproducibility and thus have issued policies requiring researchers to share their research artifacts with the scientific community."
---

Anyone working in an organization that supports or engages in scientific research has likely encountered discussions about reproducibility.  In the past decade, various research stakeholders have become more and more insistent in their calls for data sharing and research transparency as a means of upholding the credibility of the scientific outputs.  This episode engages in these discussions and illustrates the various reasons behind demands for reproducibility, beginning with an exploration of the term, “reproducibility.”

## Defining "Reproducibility"  
  
Reproducibility, which has emerged as a standard-bearer for scientific integrity, considers what happens when a research study is repeated.  For example, a researcher discovers an article that reports study findings, and then decides to conduct the same study to test whether or not the results will be consistent in a subsequent iteration of the study. If the results from the repeated study corroborate those of the original study, then the results in the published article can be considered reproducible. 

However, the term “reproducibility” carries important assumptions about the nature of the repeated study.  In some contexts, the assumption is that the repeated study applied the same methods and analyzed the same data used by the original study investigator.  In other contexts, reproducibility implies that either the original methods or the original data, but not both, were used to assess the integrity of results. 

To disambiguate these various meanings, we specify three types of reproducibility that articulate the primary distinctions among the various conceptions of reproducibility defined by [Victoria Stodden (2015)](https://doi.org/10.1146/annurev-statistics-010814-020127): *empirical reproducibility*, *statistical reproducibility*, and *computational reproducibility*.  

### Empirical Reproducibility

**original methods + new data**

Empirical reproducibility assumes that there is comprehensive documentation of research methods and protocols to follow, and this allows for subsequent studies to follow those same research methods and protocols to collect and analyze data to yield results that corroborate those reported by the original investigators. 

In animal studies, repeating experiments to demonstrate empirical reproducibility is expected. This requires standardization of experimental conditions to ensure that inconsistencies in study protocols are not the cause of inconsistencies in results. For mice experiments, this includes the use of lab-specified cage types and temperature, cage cleaning schedules, feeding protocols, etc.  Despite careful adherence to standards, it is known that one often overlooked detail can affect the empirical reproducibility of experimental results--the experimenter. For reasons yet to be fully understood, differences among experimenters such as gender and attitude may introduce enough variance in experimental conditions that are the cause of empirical irreproducibility.  

### Statistical Reproducibility

**new methods + original data**

Statistical reproducibility relies on the application of appropriate statistical methods to yield defensible results. Studies that suffer from statistical irreproducibility have weaknesses in the statistical methods and analysis, which precludes the possibility of repeating the study and yielding the same results.  

Because of the impossibility of studying perpetually-changing conditions of the Earth’s climate system, climate scientists test the reliability of their global temperature projections using a coordinated model intercomparison strategy. With this strategy, researchers run different computational models using the same data inputs and then compare the results produced by each model.  Agreement among models demonstrates statistical reproducibility, which suggests the reliability of results. Disagreement, on the other hand, may indicate misapplication of model algorithms or problematic model design indicative of statistical irreproducibility.

### Computational Reproducibility

**original methods + original data**

Computational reproducibility considers scientific practice that relies on computational methods to produce results. Simply put, it is the ability to use the original data and code to produce identical results as those of the original study.

The discovery of a single flaw in programming scripts used to analyze chemistry data called into question over 100 published studies. The issue was a module included in the script that required use of a specific operating system to execute calculations to produce the correct results. Researchers realized this only when they noticed inconsistent results when running the scripts in different computing environments. The inconsistencies, which demonstrate computational irreproducibility, were significant enough to prompt researchers to reconsider the results of their published studies.
<br>
<br>
**Suggested reading:**  
Stodden, V. (2015). Reproducing statistical results. *Annual Review of Statistics and Its Application, 2*(1), 1–19. [https://doi.org/10.1146/annurev-statistics-010814-020127](https://doi.org/10.1146/annurev-statistics-010814-020127)

> ## Spotlight: Reproducibility vs. Replicability
>
> In discussions of reproducibility, you also may have seen the term replicability used to describe any one of the three definitions provided above.  The terms reproducibility and replicability have been used interchangeably and with conflating definitions, ultimately obfuscating their intended meanings.  However, it does seem that the scientific community is converging on clearer definitions that capture the nuances of these related terms.
>
> A recent report published by the National Academies of Sciences, Engineering and Medicine (2019) makes a clear distinction between reproducibility and replicability as a means to resolve ambiguities in the use of these and related terms.  Their definitions are below as presented in the report:  
>   <br>
> > *Reproducibility* is obtaining consistent results using the same input data; computational steps, methods, and code; and conditions of analysis. This definition is synonymous with “computational reproducibility[.]”
> >
> > *Replicability* is obtaining consistent results across studies aimed at answering the same scientific question, each of which has obtained its own data (p. 46).
>
> **Suggested reading:**  
> National Academies of Sciences, Engineering, and Medicine. (2019). *Reproducibility and replicability in science*. National Academies Press. [https://doi.org/10.17226/25303](https://doi.org/10.17226/25303)
{: .callout}

The following challenge offers an opportunity to apply the definitions of the three types of reproducibility to real-world scenarios. Exploring these scenarios will help to solidify our understanding of the nuances among the reproducibility types and their definitions, and to see how irreproducibility can play out.

> ## Exercise: Reproducibility, Reproducibility, Reproducibility
>
> Read the descriptions of real-life instances in which published research findings were discovered to be non-reproducible. Based on the definitions of reproducibility types, determine which—**empirical**, **statistical**, or **computational**—applies to the scenario in each description.
> 
> **Scenario 1: Slicing and Dicing Food Data**  
> If you believe that shopping hungry compels you to make poor food purchasing decisions or that the size of your plate can influence how much you eat, you have a single university-based food lab to thank. Over the past three decades, the principal investigator (PI) of this renowned lab had over 250 articles published describing results of studies of food-related behavior, many of which have entered the popular imagination through mainstream media outlets. Some of these studies informed the USDA’s Center for Nutrition Policy and Promotion, which issues dietary guidance for the National School Lunch Program, Supplemental Nutrition Assistance Program (SNAP), and other federally sponsored nutrition programs.
>
> A closer look at the lab’s research by other scientists and statisticians, however, revealed considerable problems that would prevent them from repeating the analyses of published works. What they discovered was rampant p-hacking, a dubious practice in which statistical tests are run repeatedly on a dataset in an attempt to yield statistically significant results, irrespective of the research question or hypothesis—if any—at hand.  Beyond p-hacking, scientists also found calculation errors including unfeasible means and standard deviations. This was, perhaps, no accident, as evidenced by an email from the PI to a lab member that instructed her to dig through a dataset to find significant relationships among variables, writing, “I don’t think I’ve ever done an interesting study where the data ‘came out’ the first time I looked at it.” A few years later after these discoveries were made, several of the PI’s publications were retracted and an academic misconduct investigation prompted his removal from teaching and research duties at the university.
>
> **Scenario 2:  Excel Fail**  
> In 2013, a graduate student at the University of Massachusetts Amherst was assigned a class project to select an article from an economics journal and attempt to reproduce its findings. After several attempts, the student was unsuccessful, assuming that he had made some mistake in his own analysis. Even after obtaining the underlying analysis data from the well-respected authors themselves, he was still unable to reproduce the results. Upon closer inspection of the spreadsheet of data he was given, however, he found a critical discovery that would shock the entire field of economics.
>
> That discovery was a basic Excel miscalculation, one that tested the veracity of the findings from the influential article that was cited over 4,000 times and used by governments to justify specific austerity measures to address economic crises. While corrections to the analysis yielded different results (which the student later published) from those in the original article, the authors insisted that these differences did not change their central findings. They did, however, acknowledge their error in a public statement: “It is sobering that such an error slipped into one of our papers despite our best efforts to be consistently careful. We will redouble our efforts to avoid such errors in the future.”
>
> **Scenario 3:  Power(less) Pose**  
> With over 60,000 online views, one of the most popular TED Talks convinced many people that “power posing” induces an actual sense of increased power. The presenter, a social psychologist, shared the results of a study she published along with two of her colleagues that investigated the physiological and behavioral effects of posing in open, expansive postures: wide stance, hands on hips. The authors found that embodiments of power (i.e., power poses) cause a decrease of cortisol (the stress hormone) while increasing testosterone and risk tolerance. Based on these observations, they concluded that power posing manifests actual feelings of power.
>
> After other scientists repeated the study and failed to yield comparable results that could demonstrate the robustness of the original power pose findings, some in the scientific community cast doubt on the soundness of the original study design and protocols. One of the most vocal skeptics was one of the co-authors of the original study, who later announced that “I do not believe that ‘power pose’ effects are real.” Aside from the small sample size and a questionable participant selection process, he explained that the experiment involved male and female participants (not distinguished by gender) who performed risk-taking tasks and subsequently were informed that they had won small cash prizes. Because the act of winning increases testosterone levels, there was no way to determine whether the increase in testosterone was an effect of the power pose as the paper concluded, or if it was merely an effect of winning. Despite this controversy, studies on power posing continue--with varying results.
>
> > ## Solution
> >
> > **Scenario 1 (Slicing and Dicing Food Data):  Statistical Reproducibility**  
> > In this scenario, research results were generated using an inappropriate, dubious statistical technique. Statistical analyses were also rife with errors and miscalculations, which would make it impossible for anyone to arrive at the same results. This example demonstrates lack of *statistical reproducibility*.
> > 
> > **Scenario 2 (Excel Fail):  Computational Reproducibility**  
> > In this scenario, the student attempted to reproduce the findings in a journal article by using the authors’ own data used to generate the results reported in the article. Unfortunately, Herndon was unable to do so, which demonstrates a failure to *computationally reproduce* the published results.
> >
> > **Scenario 3 (Power(less) Pose):  Empirical Reproducibility**  
> > In this scenario, researchers repeated the steps of the original power pose experiment but arrived at different results. Problems with the study design and protocols rendered the original power pose study *empirically irreproducible*.
> {: .solution}
{: .challenge}

> ## Spotlight: What About Qualitative Research?
>
> Qualitative research methodologies do not rely on analyses of quantitatively measurable variables (other than research that transforms qualitatively derived data into quantitatively analyzable data, e.g., text mining, natural language processing), which is why some scholars have argued that reproducibility standards do not or cannot apply to qualitative research. There is no doubt, however, that findings from qualitative studies must be subject to the same level of scrutiny as those produced by their quantitative counterparts. Certainly, the credibility of qualitative research is just as important as the credibility of quantitative research.  Assessing the reproducibility of qualitative research is conceivable, albeit with a focus on **transparency**.
> 
> Considering the more constructivist nature of most qualitative research (in contrast to positivist quantitative research), assessments of research integrity emphasize *production transparency* and *analytic transparency*.  Production transparency requires that the processes for research participant selection, data collection, and analytic interpretation—and the decisions that informed these processes—be documented in explicit detail.  Analytic transparency demands clear descriptions and explanations of the methods and logic used to draw conclusions from the data.  For qualitative research, a high degree of production and analytic transparency is prerequisite for demonstrating research rigor and credibility.
>
> <br>
> **Suggested readings:**<br>
> Elman, C., Kapiszewski, D., & Lupia, A. (2018). Transparent social inquiry: Implications for social science. *Annual Review of Political Science, 21*, 29–47. [https://doi.org/10.1146/annurev-polisci-091515-025429](https://doi.org/10.1146/annurev-polisci-091515-025429)
> 
> TalkadSukumar, P., & Metoyer, R. (2019). Replication and transparency of qualitative research from a constructivist perspective [Preprint]. Open Science Framework. [https://doi.org/10.31219/osf.io/6efvp](https://doi.org/10.31219/osf.io/6efvp)
{: .callout}

## The Impetus for Scientific Reproducibility

To appreciate the importance of scientific reproducibility, consider the belief that autism is linked to vaccines. This notion first appeared in a 1998 article by Andrew Wakefield and his colleagues, who reported results of a study of a small group of children who had received the MMR vaccine and were later diagnosed with autism.  A subsequent examination of the study protocols and data from health records, however, revealed that no interpretation of the data could have reasonably concluded that instances of autism diagnoses were linked to the vaccine. The Wakefield articles eventually were retracted by the *Lancet* journal that published them, and Wakefield was found guilty of scientific misconduct and fraud.  Our understanding of the relationship between autism and vaccines is more reliably supported by the many studies and meta-analyses of studies on the subject that have consistently shown that vaccines do not cause autism. 

For scientific claims to be credible, they must be able to stand up to scrutiny, which is a hallmark of science. The scientific community promotes the credibility of its claims through systems of peer review and research replication. Confirmation of the reproducibility of research results adds another necessary element of research checks and balances, particularly with scientific research increasingly becoming computationally intensive.  **The ability of a researcher to obtain and use the data and analysis code from the author of published scientific findings to reproduce those findings independently is an essential standard by which the scientific community can judge the integrity of the scientific record.** 

Despite the vaccine-autism link having been disproven, Wakefield’s research continues to be cited in anti-vaccine campaigns that spread misinformation and disinformation about so-called dangers of vaccines.  Such campaigns have contributed to vaccine hesitancy, which has hindered public health initiatives to reduce the spread of pandemic diseases through vaccination. This example underscores the importance of recent calls for reproducibility as a precondition of scientific publication.
<br>
<br>
**Suggested readings:**  
Motta, M., & Stecula, D. (2021). Quantifying the effect of Wakefield et al. (1998) on skepticism about MMR vaccine safety in the U.S. *PLOS ONE, 16*(8), e0256395. [https://doi.org/10.1371/journal.pone.0256395](https://doi.org/10.1371/journal.pone.025639) 

Ullah, I., Khan, K. S., Tahir, M. J., Ahmed, A., & Harapan, H. (2021). Myths and conspiracy theories on vaccines and COVID-19: Potential effect on global vaccine refusals. *Vacunas, 22*(2), 93–97. [https://doi.org/10.1016/j.vacun.2021.01.001](https://doi.org/10.1016/j.vacun.2021.01.001)

## The Reproducibility Mandate

There are plenty of high-profile examples of research that were found to be irreproducible, prompting the question of whether or not science is experiencing a “reproducibility crisis.”  Recent studies to determine the extent to which published research is or is not reproducible have been concerning to many given that investigators were unable to successfully reproduce findings from a significant portion of the published research examined by investigators.

In a [2016 survey conducted by the journal *Nature*](https://doi.org/10.1038/533452a), researchers were asked if there was a reproducibility crisis in science.  Of the 1,576 who responded to the survey, 90% agreed that there was at least a slight crisis. 70% conceded that they were unable to reproduce a study conducted by another scientist, with over half admitting to being unable to reproduce a study that they, themselves, conducted!
 
**The reasons for irreproducibility are plenty, but the issues that appear quite often are the result of scientific practices that overlook the data management and curation activities**: missteps in analysis workflows due to gaps in documentation, ethical and/or legal violations of non-anonymized human subjects data or redistribution of restricted proprietary data, code execution failures because of computing environment mismatches, inconsistent analysis outputs from use of the wrong data file versions, and lack of access of data and code to reproduce results. Despite these seemingly minor issues, the repercussions can be serious.

> ## Spotlight: Yet Another Term: “Preproducibility”
>
> In a 2018 article published in the journal *Nature*, Phillip Stark offered another term for consideration for use in discussions of reproducibility:  **preproducibility**.  He wrote, “An experiment or analysis is preproducible if it has been described in adequate detail for others to undertake it.  Preproducibility is a prerequisite for reproducibility…” (p. 613).  The question of reproducibility, according to Stark, is irrelevant if documentation of research methods and protocols are insufficient or unavailable.  Stark declared his unequivocal stance on the subject, declining to review any manuscript that is not preproducible.   
> 
> Read the article that introduces the concept of preproducibility here:<br>
> **Stark, P. B. (2018). Before reproducibility must come preproducibility. *Nature, 557*(7707), 613–613. [https://doi.org/10.1038/d41586-018-05256-0](https://doi.org/10.1038/d41586-018-05256-0)**
{: .callout}

Perhaps with the so-called reproducibility crisis in mind, various research stakeholders have taken steps to promote and protect the integrity of scientific research by issuing policies and/or guidelines that require researchers to perform data management tasks to ensure data are accessible and usable. This includes the funding agencies that support research initiatives, scholarly journals that publish the scientific record, and academic societies that establish standards for research conduct. 

### Funding Agencies

Funding agencies make billions of dollars in scientific investments by sponsoring grant programs that provide support to research projects. To maximize their investments, many funders have issued policies that require grant awardees to make the materials produced in the course of funded research activities publicly available.  By doing so, the scientific community can reuse datasets, analysis code, and other research artifacts to extend and verify results.  Below are examples of funding agencies that have data policies in place.

| Funding Agency | Summary |
| -------------- | ------- |
| [Alfred P. Sloan Foundation](https://sloan.org/storage/app/media/files/application_documents/Sloan-Grant-Proposal-Guidelines-Research-Projects.pdf) | "Scientific progress depends on the sharing of information, on the replication of findings, and on the ability of every individual to stand of the shoulders of her predecessors...potential grantees are asked to attend to the outputs their research will create and how those outputs can best be put in service to the larger scientific community."|
| [Institute for Museum and Library Services (IMLS)](https://www.imls.gov/sites/default/files/digitalproduct.pdf) | "The digital products you create with IMLS funding require effective stewardship to protect and enhance their value, and they should be freely and readily available for use and reuse by libraries, archives, museums, and the public." |
| [NASA](https://science.nasa.gov/earth-science/earth-science-data/data-information-policy/data-rights-related-issues) | "...scientific data product algorithms and data products or services produced through the [Earth Science] program shall be made available to the user community on a nondiscriminatory basis, without restriction, and at no more than the marginal cost of fulfilling user requests." |
| [National Institutes of Health (NIH)](https://sharing.nih.gov/data-management-and-sharing-policy/about-the-data-management-sharing-policies) | "The National Institutes of Health (NIH) Policy for Data Management and Sharing (herein referred to as the DMS Policy) reinforces NIH's longstanding commitment to making the results and outputs of NIH-funded research available to the public through effective and efficient data management and data sharing practices." |
| [National Science Foundation (NSF)](https://www.nsf.gov/bfa/dias/policy/dmp.jsp) | "Investigators are expected to share with other researchers, at no more than incremental cost and within a reasonable time, the primary data, samples, physical collections and other supporting materials created or gathered in the course of work under NSF grants. Grantees are expected to encourage and facilitate such sharing." |

### Scholarly Journal Publishers

As stewards of the scientific record, journals bear responsibility for ensuring that the articles they publish contain verifiable claims.  Moreover, journals recognize the role they play in traditional tenure and promotion structures, which appraise scientific productivity based on publication of articles in scholarly journals.  Thus, journal policies that make publication contingent on data sharing and verification are considered a promising tool for advancing research reproducibility. Below are examples of journals with rigorous data policies.

| Scholarly Journal | Summary |
| ----------------- | ------- |
| [American Journal of Political Science (AJPS)](https://ajps.org/ajps-verification-policy/) | "The corresponding author of a manuscript that is accepted for publication in the *American Journal of Political Science* must provide materials that are sufficient to enable interested researchers to verify all of the analytic results that are reported in the text and supporting materials...When the draft of the manuscript is submitted, the materials will be verified to confirm that they do, in fact, reproduce the analytic results reported in the article." |
| [American Economic Association (AEA) Journals](https://www.aeaweb.org/journals/data/data-code-policy) | "Authors of accepted papers that contain empirical work, simulations, or experimental work must provide, prior to acceptance, information about the data, programs, and other details of the computations sufficient to permit replication, as well as information about access to data and programs...The AEA Data Editor will assess compliance with this policy, and will verify the accuracy of the information prior to acceptance by the Editor." |
| [eLife](https://reviewer.elifesciences.org/author-guide/journal-policies) | "Regardless of whether authors use original data or are reusing data available from public repositories, they must provide program code, scripts for statistical packages, and other documentation sufficient to allow an informed researcher to precisely reproduce all published results." |
| [Personality Science](https://ps.psychopen.eu/index.php/ps/open-science) | "*Personality Science* (PS) takes good, transparent, reproducible, and open science very seriously. This means that all published papers will have underwent screening regarding to what extent they have fulfilled Transparency and Openness Promotion (TOP) Guidelines." |
| [Science](https://www.science.org/content/page/science-journals-editorial-policies#research-standards) | "All data used in the analysis must be available to any researcher for purposes of reproducing or extending the analysis...In general, all computer code central to the findings being reported should be available to readers to ensure reproducibility...Materials/samples used in the analysis must be made available to any researcher for purposes of directly replicating the procedure." |

### Academic Societies

Academic societies have taken up the issue of reproducibility in updated professional codes of conduct or ethics.  Citing responsibility to advance research in their discipline, these formal documents obligate researchers to enable others to evaluate their knowledge claims through transparent research practices and public access to data and materials underlying those knowledge claims. Below is a list of academic societies that have issued policies or statements promoting data access and research transparency.

| Academic Society | Summary |
| ---------------- | ------- |
| [American Geophysical Union (AGU)](https://www.agu.org/-/media/Files/AGU-Data-Position-Statement-Final-2015.pdf) | "The cost of collecting, processing, validating, documenting, and submitting data to a repository should be an integral part of research and operational programs. The AGU scientific community should recognize the professional value of such activities."|
| [American Psychological Association (APA)](https://www.apa.org/ethics/code) | "After research results are published, psychologists do not withhold the data on which their conclusions are based from other competent professionals who seek to verify the substantive claims through reanalysis and who intend to use such data only for that purpose, provided that the confidentiality of the participants can be protected and unless legal rights concerning proprietary data preclude their release."|
| [American Sociological Association (ASA)](https://www.acm.org/code-of-ethics) | "Consistent with the spirit of full disclosure of methods and analyses, once findings are publicly disseminated, sociologists permit their open assessment and verification by other responsible researchers, with appropriate safeguards to protect the confidentiality of research participants...As a regular practice, sociologists share data and pertinent documentation as an integral part of a research plan." |

{% include links.md %}
