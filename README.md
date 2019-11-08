
<!-- README.md is generated from README.Rmd. Please edit that file -->

# SAWpaper: Self-Assessment Works Paper

<!-- badges: start -->

[![Lifecycle:
experimental](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://www.tidyverse.org/lifecycle/#experimental)
[![CRAN
status](https://www.r-pkg.org/badges/version/cstatops)](https://CRAN.R-project.org/package=SAWpaper)
<!-- badges: end -->

This package and corresponding GitHub repository are intended to enhance
the reproducibility of a research paper. The principal investigators for
the study are Dr. Paula Winke (Associate Professor) and Dr. Susan Gass
(University Distinguished Professor), both of whom belong to the
Department of Linguistics & Germanic, Slavic, Asian, and African
Languages at Michigan State University. The paper analyzes data on
Spanish language learners who took a Can-Do self-assessment test, along
with the more authoritative OPIc language proficiency test. We did both
correlation analyses and continuation-ratio models that examine the
effect of course and OPIc speaking proficiency scores on the passing
rate for each level of the Can-Do statements self-assessment. The
objective was to validate the Can-Do test results.

## Task List

  - Add disclaimer text regarding our results not being the official
    position of the funder?
  - Add more details about downloading and installing the repository.

## Associated Research Paper

Winke, P., Zhang, X., & Pierce, S. J. (2019). *Self-assessment works\!
Continuation-ratio models for testing course and OPIc score effects on
oral proficiency self-assessments*. Michigan State University, East
Lansing, MI. Manuscript in preparation.

## Funding Sources

Funding for this research was provided by the following grants.

Winke, P., Gass, S., & Pierce, S. J. (08/01/2017-07/31/2018). Michigan
State University Language Flagship Proficiency Initiative Year 4
continuation proposal. \[Award \#: 0054-MSU-22-PI-280-PO2, $249,865\].
Sponsor: Institute of International Education. Location: Michigan State
University, East Lansing, MI.

Winke, P., Gass, S., & Pierce, S. J. (01/01/2019–12/31/2019). Michigan
State University Language Flagship Proficiency Initiative Year 5
continuation proposal. \[Award \#: 0054-MSU-22-PI-280-PO2, Awarded,
$37,634\]. Sponsor: Institute of International Education. Location:
Michigan State University, East Lansing, MI.

## Software Environment

We use R Markdown to enhance reproducibility. Knitting an R Markdown
script can generate a PDF file containing explanatory text, R code, plus
R output (text and graphics), although it can also produce HTML or
Markdown files too depending on the contents of the R Markdown file.

  - We use [RStudio (version 1.2.5001 or later)](www.rstudio.org) to
    work with R and R markdown files. The software chain looks like
    this: **Rmd file -\> RStudio -\> R -\> knitr -\> pandoc -\> MiKTeX
    -\> PDF file**.
  - We are using [MiKTeX version 2.9](https://miktex.org) to compile
    LaTeX files into PDF files.

## Installation

This package is only available from a *private* repository available on
[GitHub](https://github.com/). It is private for now because we are not
ready to release this code yet.

The package can be installed with the code shown below. If you don’t
have *devtools* installed, uncomment that line first.

``` r
# install.packages("devtools")
devtools::install_github("sjpierce/SAWpaper")
```

### Downloading The Repository from GitHub

### Installing the Repository from a Compressed File

## Repository Contents

This repository contains data files, the R markdown scripts used to
analyze them, plus the output from when we ran the scripts. There is
considerably more raw statistical output than we could put directly into
the resulting manuscript. That is preserved here for the sake of
reproducibility and completeness of reporting. We also include other
files necessary to work with the repository in RStudio and GitHub and to
build the R package from the repository files.

## Data File Documentation

There are some data files included in this repository. The are located
in the *data* folder and stored as comma separated values in text files
(i.e., .csv files). We briefly describe the contents of each file below.

``` r
# Load some useful packages.
library(here)
#> here() starts at C:/Users/Steve/Documents/CSTAT/Clients/Winke_Paula/18-009/SAWpaper
library(knitr)

# Read in the included data files. 
df_corr <- read.csv(here::here("./data/DF_CORR.csv"))
df_crm  <- read.csv(here::here("./data/DF_CRM.csv"))
```

### Learner Data File: *data/DF\_CORR.csv*

This data file has one row per Spanish language learner in our study,
with \(N = 820\) observations and 5 variables. The first few rows of
data are shown below.

``` r
# Display top few rows of df_corr.
kable(head(df_corr))
```

| id | Course | OPIc | OPIC | Level |
| -: | -----: | :--- | ---: | ----: |
|  1 |    400 | IH   |    6 |     1 |
|  2 |    100 | NH   |    3 |     1 |
|  3 |    200 | IL   |    4 |     2 |
|  4 |    300 | IM   |    5 |     2 |
|  5 |    200 | NM   |    2 |     1 |
|  6 |    200 | NH   |    3 |     1 |

This is the data file to use when examining simple correlations between
variables like OPIC and Course. The variables are described below.
Remember that R is case-sensitive with variable names, so OPIc and OPIC
are different (but related) variables.

  - *id*: An anonymized participant identification number. Each learner
    has a unique id value. The values are integer numbers.

  - *Course*: The level of the Spanish language course the learner was
    taking at the time of taking the self-assessment test. First year
    courses are coded 100, second year courses are coded 200, third year
    courses are coded 300, and fourth year courses are coded 400. Course
    values are stored as integers.

  - *OPIc*: These two-character alphabetic codes are values for scores
    on the American Council on the Teaching of Foreign Languages (ACTFL)
    Oral Proficiency Interview - Computer (OPIc) test for Spanish
    language proficiency. The possible scores, in increasing level of
    proficiency, are:
    
      - *NL*: Novice low.
      - *NM*: Novice mid.
      - *NH*: Novice high.
      - *IL*: Intermediate low.
      - *IM*: Intermediate mid.
      - *IH*: Intermediate high.
      - *AL*: Advanced low.
      - *AM*: Advanced mid.
      - *AH*: Advanced high.
      - *S*: Superior (which does not occur in thie dataset).

  - *OPIC*: These integer values are a simple recode of the OPIc
    variable. The possible scores, in increasing level of proficiency,
    are:
    
      - *1*: Novice low.
      - *2*: Novice mid.
      - *3*: Novice high.
      - *4*: Intermediate low.
      - *5*: Intermediate mid.
      - *6*: Intermediate high.
      - *7*: Advanced low.
      - *8*: Advanced mid.
      - *9*: Advanced high.
      - *10*: Superior (which does not occur in thie dataset).

  - *Level*: These integer values show the maximum level the learner
    reached on the self-assessment test based on 50 Can-Do statements.
    There are five possible levels (1 through 5), with higher values
    indicating greater self-assessed proficiency.

### Level-Transition Test Data File: *data/DF\_CRM.csv*

This data file has one row per level transition test attempted by a
learner in our study, with \(N = 1340\) observations and 5 variables.
The first few rows of data are shown below.

``` r
# Display top few rows of df_crm.
kable(head(df_crm))
```

| id | Course | COPIC | Level | pass |
| -: | -----: | ----: | ----: | ---: |
|  1 |    400 |     1 |     1 |    0 |
|  2 |    100 |   \-2 |     1 |    0 |
|  3 |    200 |   \-1 |     1 |    1 |
|  3 |    200 |   \-1 |     2 |    0 |
|  4 |    300 |     0 |     1 |    1 |
|  4 |    300 |     0 |     2 |    0 |

This dataset is used in continuation-ratio modeling of the
self-assessment test results. The data shown above have two rows for id
= 3. They show that this learner passed the level transition test to get
from level 1 to level 2, but failed to pass the transition test to get
from level 2 to level 3. The variables are described in more detail
below.

  - *id*: An anonymized participant identification number. Each learner
    has a unique id value. The values are integer numbers.

  - *Course*: The level of the Spanish language course the learner was
    taking at the time of taking the self-assessment test. First year
    courses are coded 100, second year courses are coded 200, third year
    courses are coded 300, and fourth year courses are coded 400. Course
    values are stored as integers.

  - *COPIC*: These integer values are a centered version of the OPIC
    variable found in *df\_corr*. The centering was done around OPIC =
    5, so the centered scores, in increasing level of proficiency, are:
    
      - *-4*: Novice low.
      - *-3*: Novice mid.
      - *-2*: Novice high.
      - *-1*: Intermediate low.
      - *0*: Intermediate mid.
      - *1*: Intermediate high.
      - *2*: Advanced low.
      - *3*: Advanced mid.
      - *4*: Advanced high.
      - *5*: Superior (which does not occur in thie dataset).

  - *Level*: These integer values show which level transition test from
    the Can-Do self-assessment the learner was attempting pass on a
    given row of data. There are four possible level transition tests:
    
      - *1*: Transition from level 1 to level 2.
      - *2*: Transition from level 2 to level 3.
      - *3*: Transition from level 3 to level 4.
      - *4*: Transition from level 4 to level 5.

  - *pass*: This binary integer variable is coded 0 when the learner did
    not pass the level transition test shown in the Level variable, and
    1 when the learner pased the test.
