---
title: Understanding Displacement from Hurricane Katrina; Risk Factors, Health, and
  Wellbeing Outcomes
author: "Emily Cobb"
date: "2023-12-15"
output: pdf_document
---

    ## -- Attaching core tidyverse packages ------------------------ tidyverse 2.0.0 --
    ## v dplyr     1.1.3     v readr     2.1.4
    ## v forcats   1.0.0     v stringr   1.5.0
    ## v ggplot2   3.4.4     v tibble    3.2.1
    ## v lubridate 1.9.3     v tidyr     1.3.0
    ## v purrr     1.0.2     
    ## -- Conflicts ------------------------------------------ tidyverse_conflicts() --
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()
    ## i Use the conflicted package (<http://conflicted.r-lib.org/>) to force all conflicts to become errors
    ## here() starts at /Users/emily/eds222/eds222-final-project
    ## 
    ## Loading required package: carData
    ## 
    ## lattice theme set by effectsTheme()
    ## See ?effectsTheme for details.
    ## 
    ## corrplot 0.92 loaded
    ## 
    ## Registered S3 method overwritten by 'geojsonsf':
    ##   method        from   
    ##   print.geojson geojson
    ## 
    ## 
    ## Attaching package: 'geojsonio'
    ## 
    ## 
    ## The following object is masked from 'package:base':
    ## 
    ##     pretty
    ## 
    ## 
    ## Suggested APA citation: Thériault, R. (2023). rempsyc: Convenience functions for psychology. 
    ## Journal of Open Source Software, 8(87), 5466. https://doi.org/10.21105/joss.05466

    ## Rows: 344 Columns: 46
    ## -- Column specification --------------------------------------------------------
    ## Delimiter: ","
    ## chr  (3): EVENTCODEDATE, evac.state, state.most.time
    ## dbl (42): caseid, name_indicator, eventcode, sex, age, pre_marriagestat, cur...
    ## lgl  (1): mobile
    ## 
    ## i Use `spec()` to retrieve the full column specification for this data.
    ## i Specify the column types or set `show_col_types = FALSE` to quiet this message.

## Introduction

As an Anthropologist, my central research focuses on the biological embodiment of environmental conditions, and how this embodiment affects overall health and wellbeing, both mental and physical. My main topics consist of the pathways and biological mechanisms in which this embodiment happens, understanding the larger circumstances causing environmental/biological stressors is becoming increasingly important. I also have interests in how environmental stressors inflict life change based on personal experience, and how these stressors can either lead to differing health outcomes. Long term, I want to examine resilience factors in this context, to understand what factors help decrease negative health outcomes in hopes of developing interventions. For the following project, I am working on the effects of natural disaster based displacement, examining risk factors for displacement and if displaced groups different in their mental and perceived overall health outcomes. As climate change is increasing the amount of natural disasters and increasing potential to induce large scale population movement (Oliver-Smith, 2009; McCarney & Kent 2020), understanding displacement from these events as a psychosocial stressor is necessary to be able to combat it and improve population health in times of uncertainty. Address risk factors of being in a displaced group also helps target interventions to those who may be more at risk. 

    To attempt to answer this question, I will be working with data from the Displaced New Orleans Residents pilot study. This data is publicly available and focuses on New Orleans (NO) residents who experienced Hurricane Katrina (HK) in 2005. Unfortunately, the data from the following study is only available upon request and I was not able to obtain access for this project. The pilot study data consists of survey data collected by phone, visits, and through mail throughout 2006, targeting residents in areas of the city affected by damage from HK. As the frequency of strong hurricanes (category 4/5) are theorized to increase (D. K. Cobb, Personal Communication, December 7, 2023) along with climate change, understanding hurricane related displacement in coastal areas is a target area for research on anticipated displacement.  Survey questions included sociodemographic factors, hurricane impact related scales, and evacuation and displacement measures. Complete sample size for all questions is n = 131. Data does not contain any time series or real spatial points for neighborhood related analyses, aside from state evacuated to, preventing time series or spatial analysis techniques. 

    A growing body of work on natural disaster displacement patterns contends with the corresponding effect of displacement on mental health outcomes. In 1991, Morrow-Jones H. & Morrow-Jones C. (1991) report that there are significant differences in those who move due to a natural disaster compared those who move due to unrelated reasons. They report mixed potential effects of socio-economic status (SES) on displacement outcomes, stating that higher SES is usually related to a higher success of returning. However, the measurable effect of this has been ambiguous.The effect of homeownership is also ambiguous, as homeowners have less mobility than renters, but renters have less control over fixing residence damage. It has been suggested that as homeownership is associated with higher SES, that homeowners might have better outcomes when moving becomes a necessity. Black people have also been historically affected more by displacement during natural disasters, and this has been attributed to historical segregation of neighborhoods and damage patterns in those neighborhoods (Graif, 2016)**.** Other work on HK has demonstrated these patterns, so race is expected to be a significant factor in these models (Graif, 2016). 

    Morrow-Jones H. & Morrow-Jones C. (1991) also report a high incidence of depression and increased stress levels among displaced movers compared to non-displaced movers. Swartz et al. (2018), in a study of NY residents affected by Hurricane Sandy, found that displacement was also positively associated with a higher risk of developing PTSD. This mental health impact is also unequal among groups and those experiencing severe disability, experiencing disability or being displaced into a disaster shelter both increased the risk of negative mental health effects. Burrows et al. (2021) also found that higher income reduces the negative mental effects from displacement as well. Overall, displacement has been found to increase stress levels and result in poorer mental health outcomes, but more research is needed to clarify these relationships. 

### Analysis

    Burrows et al. (2021) was used as a reference for the analyses as preformed here. Burrows et al. implemented logistic regression models with sociodemographic factors to predict displacement and Welch Two Sample T-Tests to determine differences in mental health outcomes in displaced versus non-displaced groups. 

#### Multivariate Logistic Regression

    Burrows et al. (2021) examined displacement due to landslides in Indonesia, so while there is variability in data structure between their dataset and this one, I am their approach of using a binary outcome variable. I\'ve created a binary outcome variable based on whether the individual in the sample relocated after HK or did not relocated (moved back or did not evacuate originally.) As for predictors, sociodemographic factors will be included as control variables, along with housing data, state moved to, and damage to residence from HK. Variables included were motivated by previous literature as described above. A model with an interaction effect between renting or owning and damage to residence is included to try and access the differing effect of residence damage based on ownership.The aim of this model is to identify risk factors associated with a higher probability of displacement to characterize displaced versus non displaced groups. 

#### Welch Two Sample T-tests

    Three t-tests were also ran to determine if significant differences in mental health outcomes exist between displaced and non displaced groups. The first t-test compared general stress scores between these groups in response to HK, a 10 point scale with 1 being least stressed and 10 being most stressed. For the second test, a depression score was calculated from q31-36 included in the survey data, aimed at quantifying depression symptoms to compare between groups, lowest scores indicate higher depression occurrence. For the third test, a health change score was calculated from before and after self rated health measures included in the survey, and change in health was compared across groups. Negative score represents perceived decrease in health after HK, and positive scores indicate a perceived increase in health. 

### 

Results

#### Summary Tables and Figures

```{=tex}
\begin{table}

\caption{\label{tab:unnamed-chunk-3}Compairison of Sociodemogrpahic and Housing/Hurricane Displacement Variables Between Moved and Moved Back Groups}
\centering
\begin{tabular}[t]{llrrrr}
\toprule
\multicolumn{2}{c}{ } & \multicolumn{2}{c}{Moved Away (N=94)} & \multicolumn{2}{c}{Moved Back (N=52)} \\
\cmidrule(l{3pt}r{3pt}){3-4} \cmidrule(l{3pt}r{3pt}){5-6}
  &    & N & Pct. & N & Pct.\\
\midrule
Black & 0 & 42 & 44.7 & 35 & 67.3\\
 & NA & 52 & 55.3 & 17 & 32.7\\
Hispanic & 0 & 0 & 0.0 & 1 & 1.9\\
 & NA & 94 & 100.0 & 51 & 98.1\\
White & 1 & 50 & 53.2 & 15 & 28.8\\
 & NA & 44 & 46.8 & 37 & 71.2\\
Level of School Completed & 1 & 3 & 3.2 & 3 & 5.8\\
 & 2 & 8 & 8.5 & 7 & 13.5\\
 & 3 & 17 & 18.1 & 13 & 25.0\\
 & 4 & 19 & 20.2 & 13 & 25.0\\
 & 5 & 18 & 19.1 & 8 & 15.4\\
 & 6 & 28 & 29.8 & 8 & 15.4\\
 & 1 & 54 & 57.4 & 24 & 46.2\\
Employed Part-Time & 0 & 5 & 5.3 & 3 & 5.8\\
 & NA & 89 & 94.7 & 49 & 94.2\\
Self Employed Full-Time & 0 & 7 & 7.4 & 3 & 5.8\\
 & NA & 87 & 92.6 & 49 & 94.2\\
Self Employed Part-Time & 0 & 3 & 3.2 & 1 & 1.9\\
 & NA & 91 & 96.8 & 51 & 98.1\\
Laid off from Job & 0 & 1 & 1.1 & 1 & 1.9\\
 & NA & 93 & 98.9 & 51 & 98.1\\
Unemployed & 0 & 2 & 2.1 & 2 & 3.8\\
 & NA & 92 & 97.9 & 50 & 96.2\\
Disabled & 0 & 6 & 6.4 & 4 & 7.7\\
 & NA & 88 & 93.6 & 48 & 92.3\\
Student & 0 & 1 & 1.1 & 1 & 1.9\\
 & NA & 93 & 98.9 & 51 & 98.1\\
Own Home & 1 & 64 & 68.1 & 32 & 61.5\\
 & 2 & 30 & 31.9 & 20 & 38.5\\
 & 2 & 11 & 11.7 & 7 & 13.5\\
 & 3 & 67 & 71.3 & 32 & 61.5\\
 & 4 & 16 & 17.0 & 13 & 25.0\\
Damage to Residence & 1 & 8 & 8.5 & 17 & 32.7\\
 & 2 & 26 & 27.7 & 25 & 48.1\\
 & 3 & 49 & 52.1 & 8 & 15.4\\
 & 4 & 11 & 11.7 & 2 & 3.8\\
Income & 1 & 12 & 12.8 & 5 & 9.6\\
 & 2 & 15 & 16.0 & 8 & 15.4\\
 & 3 & 4 & 4.3 & 12 & 23.1\\
 & 4 & 13 & 13.8 & 8 & 15.4\\
 & 5 & 5 & 5.3 & 3 & 5.8\\
 & 6 & 6 & 6.4 & 3 & 5.8\\
 & 7 & 33 & 35.1 & 11 & 21.2\\
\bottomrule
\end{tabular}
\end{table}
```
### 
