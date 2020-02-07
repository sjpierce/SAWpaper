
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
  - Update the data documentation to point toward the published data
    archive at ICPSR.
  - Update `inst/SAW_Paper_Spanish_Analysis.Rmd` to integrate code from
    Xiaowan’s file `CRM_Spanish_2020-2-3.Rmd`.

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

  - We use [RStudio (version 1.2.5033 or later)](www.rstudio.org) to
    work with R and R markdown files. The software chain looks like
    this: **Rmd file -\> RStudio -\> R -\> knitr -\> pandoc -\> TinyTeX
    -\> PDF file**.
  - We recommend using [TinyTeX](https://yihui.org/tinytex/) to compile
    LaTeX files into PDF files. However, it should be viable to use
    [MiKTeX version 2.9](https://miktex.org) instead.

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
with \(N = 807\) observations and 63 variables. The first few rows of
data are shown below.

``` r
# Display top few rows of df_corr.
kable(head(df_corr))
```

| X | student\_id | Gender | Course | OPIc | OPIC | Level | Item1 | Item2 | Item3 | Item4 | Item5 | Item6 | Item7 | Item8 | Item9 | Item10 | Item11 | Item12 | Item13 | Item14 | Item15 | Item16 | Item17 | Item18 | Item19 | Item20 | Item21 | Item22 | Item23 | Item24 | Item25 | Item26 | Item27 | Item28 | Item29 | Item30 | Item31 | Item32 | Item33 | Item34 | Item35 | Item36 | Item37 | Item38 | Item39 | Item40 | Item41 | Item42 | Item43 | Item44 | Item45 | Item46 | Item47 | Item48 | Item49 | Item50 | Item1\_10 | Item11\_20 | Item21\_30 | Item31\_40 | Item41\_50 | Item1\_50 |
| -: | :---------- | :----- | -----: | :--- | ---: | ----: | ----: | ----: | ----: | ----: | ----: | ----: | ----: | ----: | ----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | --------: | ---------: | ---------: | ---------: | ---------: | --------: |
| 1 | A12479352   | Female |    100 | NL   |    1 |     1 |     1 |     2 |     1 |     1 |     3 |     1 |     2 |     2 |     1 |      1 |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |        15 |         NA |         NA |         NA |         NA |        15 |
| 2 | A12658221   | Male   |    200 | IL   |    4 |     1 |     3 |     4 |     4 |     4 |     3 |     3 |     3 |     3 |     3 |      3 |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |        33 |         NA |         NA |         NA |         NA |        33 |
| 3 | A12711564   | Female |    200 | IL   |    4 |     2 |     4 |     4 |     4 |     4 |     4 |     4 |     4 |     4 |     4 |      3 |      3 |      4 |      4 |      4 |      3 |      3 |      3 |      3 |      4 |      3 |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |        39 |         34 |         NA |         NA |         NA |        73 |
| 4 | A12879916   | Female |    200 | IM   |    5 |     5 |     4 |     4 |     3 |     4 |     4 |     4 |     4 |     4 |     4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      3 |      4 |      4 |      4 |      4 |      4 |      4 |      3 |      4 |      4 |      3 |      4 |      4 |      3 |      4 |      3 |      4 |      4 |      3 |      3 |      4 |      3 |      3 |        39 |         40 |         39 |         38 |         34 |       190 |
| 5 | A13226298   | Male   |    200 | NH   |    3 |     1 |     3 |     4 |     3 |     2 |     2 |     3 |     3 |     2 |     2 |      2 |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |        26 |         NA |         NA |         NA |         NA |        26 |
| 6 | A13320012   | Female |    200 | NM   |    2 |     1 |     3 |     3 |     4 |     4 |     3 |     3 |     3 |     3 |     2 |      3 |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |        31 |         NA |         NA |         NA |         NA |        31 |

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
learner in our study, with \(N = 1320\) observations and 66 variables.
The first few rows of data are shown below.

``` r
# Display top few rows of df_crm.
kable(head(df_crm))
```

|   X | student\_id | Gender | Course | OPIc | OPIC | COPIC | Level | pass | Item1 | Item2 | Item3 | Item4 | Item5 | Item6 | Item7 | Item8 | Item9 | Item10 | Item11 | Item12 | Item13 | Item14 | Item15 | Item16 | Item17 | Item18 | Item19 | Item20 | Item21 | Item22 | Item23 | Item24 | Item25 | Item26 | Item27 | Item28 | Item29 | Item30 | Item31 | Item32 | Item33 | Item34 | Item35 | Item36 | Item37 | Item38 | Item39 | Item40 | Item41 | Item42 | Item43 | Item44 | Item45 | Item46 | Item47 | Item48 | Item49 | Item50 | Item1\_10 | Item11\_20 | Item21\_30 | Item31\_40 | Item41\_50 | Item1\_50 | Highest\_level |
| --: | :---------- | :----- | -----: | :--- | ---: | ----: | ----: | ---: | ----: | ----: | ----: | ----: | ----: | ----: | ----: | ----: | ----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | --------: | ---------: | ---------: | ---------: | ---------: | --------: | -------------: |
|   1 | A12479352   | Female |    100 | NL   |    1 |   \-4 |     1 |    0 |     1 |     2 |     1 |     1 |     3 |     1 |     2 |     2 |     1 |      1 |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |        15 |         NA |         NA |         NA |         NA |        15 |              1 |
|   2 | A12658221   | Male   |    200 | IL   |    4 |   \-1 |     1 |    0 |     3 |     4 |     4 |     4 |     3 |     3 |     3 |     3 |     3 |      3 |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |        33 |         NA |         NA |         NA |         NA |        33 |              1 |
|   3 | A12711564   | Female |    200 | IL   |    4 |   \-1 |     1 |    1 |     4 |     4 |     4 |     4 |     4 |     4 |     4 |     4 |     4 |      3 |      3 |      4 |      4 |      4 |      3 |      3 |      3 |      3 |      4 |      3 |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |        39 |         34 |         NA |         NA |         NA |        73 |              2 |
| 810 | A12711564   | Female |    200 | IL   |    4 |   \-1 |     2 |    0 |     4 |     4 |     4 |     4 |     4 |     4 |     4 |     4 |     4 |      3 |      3 |      4 |      4 |      4 |      3 |      3 |      3 |      3 |      4 |      3 |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |        39 |         34 |         NA |         NA |         NA |        73 |              2 |
|   4 | A12879916   | Female |    200 | IM   |    5 |     0 |     1 |    1 |     4 |     4 |     3 |     4 |     4 |     4 |     4 |     4 |     4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      3 |      4 |      4 |      4 |      4 |      4 |      4 |      3 |      4 |      4 |      3 |      4 |      4 |      3 |      4 |      3 |      4 |      4 |      3 |      3 |      4 |      3 |      3 |        39 |         40 |         39 |         38 |         34 |       190 |              5 |
| 811 | A12879916   | Female |    200 | IM   |    5 |     0 |     2 |    1 |     4 |     4 |     3 |     4 |     4 |     4 |     4 |     4 |     4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      3 |      4 |      4 |      4 |      4 |      4 |      4 |      3 |      4 |      4 |      3 |      4 |      4 |      3 |      4 |      3 |      4 |      4 |      3 |      3 |      4 |      3 |      3 |        39 |         40 |         39 |         38 |         34 |       190 |              5 |

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
    variable found in *df\_corr*. We centered around Intermediate-mid
    (OPIC = 5) because it is the level of proficiency expected of
    students exiting the 200-level courses. The centered scores, in
    increasing level of proficiency, are:
    
      - *-4*: Novice low.
      - *-3*: Novice mid.
      - *-2*: Novice high.
      - *-1*: Intermediate low.
      - *0*: Intermediate mid (expected proficiency for students after
        200-level courses).
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
