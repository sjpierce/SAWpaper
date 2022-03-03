SAWpaper: Self-Assessment Works Paper Research Compendium
================
Steven J. Pierce & Xiaowan Zhang

<!-- README.md is generated from README.Rmd. Please edit that file -->
<!-- badges: start -->

[![Lifecycle:
experimental](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://www.tidyverse.org/lifecycle/#experimental)
[![CRAN
status](https://www.r-pkg.org/badges/version/cstatops)](https://CRAN.R-project.org/package=SAWpaper)
<!-- badges: end -->

This package and corresponding GitHub repository are intended to enhance
the reproducibility of a research paper by serving as a research
compendium (Marwick, Boettiger, & Mullen, 2018). The principal
investigators for the study are Dr. Paula Winke (Professor) and
Dr. Susan Gass (University Distinguished Professor), both of whom belong
to the Department of Linguistics, Languages, & Cultures at Michigan
State University. The paper analyzes data on Spanish language learners
who took a Can-Do self-assessment test, along with the more
authoritative OPIc language proficiency test. We did both correlation
analyses and continuation-ratio models that examine the effect of course
and OPIc speaking proficiency scores on the passing rate for each level
of the Can-Do statements self-assessment. The objective was to validate
the Can-Do test results.

## Task List

-   Update the data documentation to point toward the published data
    archive at ICPSR.
-   Update `inst/SAW_Paper_Spanish_Analysis.Rmd` to:
    -   Integrate code from Xiaowan’s file `CRM_Spanish_2020-2-3.Rmd`?
    -   Read data from imported .RData file rather than CSV files.
-   Copy Xiaowan’s custom functions from `CRM_Spanish_2020-2-3.Rmd` into
    R scripts under `R/` folder and add roxygen documentation to
    generate help file.
-   Fix check() warning about Undocumented data sets: ‘df_corr’
    ‘df_crm’. All user-level objects in a package should have
    documentation entries. See chapter ‘Writing R documentation files’
    in the ‘Writing R Extensions’ manual.
-   Add package citation information.

## Associated Research Paper

Winke, P., Zhang, X., & Pierce, S. J. (2021). *A closer look at a
marginalized test method: Self-assessment as a measure of speaking
proficiency* \[Manuscript submitted for publication\]. Department of
Linguistics, Languages, & Cultures, Michigan State University.

## Funding Sources

Funding for this research was provided by the following grants.

Winke, P., Gass, S., & Pierce, S. J. (08/01/2017–12/31/2018). *Michigan
State University Language Flagship Proficiency Initiative Year 4
continuation proposal* (Award #: 0054-MSU-22-PI-280-PO2) \[Grant\].
Institute of International Education.

Winke, P., Gass, S., & Pierce, S. J. (01/01/2019–12/31/2019). *Michigan
State University Language Flagship Proficiency Initiative Year 5
continuation proposal* (Award #: 0054-MSU-22-PI-280-PO2) \[Grant\].
Institute of International Education.

## Disclaimer

The opinions or points of view expressed in this research compendium and
the associated manuscript are solely those of the authors and do not
reflect the official positions of any organization or the Institute of
International Education.

## Software Environment

We use R Markdown to enhance reproducibility because it provides
excellent support for generating dynamic reports (Mair, 2016). Knitting
an R Markdown script can generate a PDF output file containing
explanatory text, R code, plus R output (text and graphics), although it
can also produce HTML or Markdown files too depending on the contents of
the R Markdown file. We have designed our scripts to produce PDF output.

-   We used the [R statistical software](https://www.r-project.org/) to
    do data management and run our analyses. You will need R to to
    reproduce our results. We recommend using the most recent stable
    release of R available from the [Comprehensive R Archive Network
    (CRAN)](https://cran.r-project.org/).
-   We used [RStudio](www.rstudio.org) 2021.9.0.351 (RStudio Team, 2021)
    to work with R and R Markdown files. RStudio is an excellent
    integrated development environment (IDE). We recommend using the
    most recent stable release available. The software chain for R
    Markdown looks like this: **Rmd file > RStudio > R > rmarkdown >
    knitr > pandoc > TinyTeX or MiKTeX > PDF file**.
-   A version of [pandoc](https://pandoc.org/) comes bundled with
    RStudio, but if you want the most recent version, download it from
    <https://pandoc.org/>.
-   We use Git (Torvalds et al., 2021) for version control, with the
    primary (i.e., main) repository hosted online by
    [GitHub](https://github.com/). For a short introduction to Git, see
    Bryan (2018). There is a longer, more detailed resource on using Git
    with R at the [Happy Git and GitHub for the
    userR](https://happygitwithr.com) website (Bryan et al., n.d.).
    Other useful resources on using Git and GitHub include Bryan
    2018. and Perez-Riverol et al. (2016). Chacon and Straub (2014) is a
          full book on using Git for version control.
-   We recommend using [TinyTeX](https://yihui.org/tinytex/) to compile
    LaTeX files produced by pandoc into PDF files. However, it may be
    viable to use [MiKTeX](https://miktex.org) instead.
-   This package depends on functions from the *piercer* package, which
    is available from a public GitHub repository at
    <https://github.com/sjpierce/piercer>. Please read and follow the
    installation instructions for *piercer* before trying to use this
    package.
-   Wickham and Bryan (n.d.) provides extensive guidance on creating R
    packages.
-   We recommend frequently updating your installed R packages.

## Installation

This *SAWpaper* package is only available from a *private* repository
available on [GitHub](https://github.com/) at
<https://github.com/sjpierce/SAWpaper>. It will remain private until we
are ready to release the code, which will likely coincide with
publication of the associated paper. After that, we will make it a
public repository.

### Obtain the Repository from GitHub

If you use Git (Torvalds et al., 2020) and have a GitHub account, either
clone or fork and clone the package to your computer using the usual Git
commands (Bryan, 2018; Bryan et al., n.d., Chapters 28 and 32).
Otherwise, manually download a ZIP file from
<https://github.com/sjpierce/SAWpaper> and unzip its contents to a
folder. Either way, the files should end up in a folder called
`SAWpaper` on your computer. That folder is your local copy of the
repository.

Note that the package code uses relative rather than absolute folder
path and file name references. Moving or renaming subfolders and/or
files may cause problems. We have tested it only with the folder
structure and file naming used in the primary repository on GitHub.

### Install the *devtools* Package from CRAN

You will need to install the [*devtools*](https://devtools.r-lib.org/)
package before you install *piercer* in the next step. You can find
*devtools* [on
CRAN](https://cran.r-project.org/web/packages/devtools/index.html) and
[on GitHub](https://github.com/r-lib/devtools). The code below will
allow you to install the current release version from CRAN.

``` r
install.packages("devtools")
```

### Install the *piercer* Package from GitHub

Please read and follow the installation instructions for *piercer* at
<https://github.com/sjpierce/piercer> before trying to use this package.

### Install the *SAWpaper* Package from GitHub

Once the steps above are done, use the following code in the R console
to install the *SAWpaper* package. This package doesn’t have any custom
functions, so this step is mostly just adds some help system
documentation and ensures that the version number for the package will
show up in the output files. Note the files this step places on your
computer will be in your personal R package library rather than in the
local repository folder.

``` r
devtools::install_github("sjpierce/SAWpaper")
```

### Install Additional R Packages from CRAN

Scripts in this R package depend on having a number of other R packages
installed. Those packages are available from CRAN and can be installed
by running the following code in the R console.

``` r
install.packages(pkgs = c("car", "directlabels", "dplyr", "fs", "ggplot2", 
                          "Hmisc", "here", "kableExtra", "knitr", "lattice", 
                          "modEVA", "multcomp", "pander", "polycor", "pROC",
                          "rmarkdown", "stringr", "texreg", "tidyr", "visreg"))
```

Once you have completed this step, you should be ready to use this
package to reproduce our results.

## Repository Contents

The diagram below shows the subfolders nested under the `SAWpaper`
folder when we last knitted the`README.Rmd file`. Individual files are
omitted. Our scripts are all designed to use path names relative to the
`SAWpaper` folder, usually by calling the `here::here()` function, which
locates the `SAWpaper` folder on your computer and fills in the path up
to that point. That increases portability of the repository.

``` r
# Load some useful packages. 
library(fs)    # for dir_tree()
library(here)  # for here()
#> here() starts at P:/Consulting/FY18/Winke_Paula/18-009/SAWpaper

# Show diagram of SAWpaper folder contents.
dir_tree(path = here(), recurse = TRUE, type = "any")
#> P:/Consulting/FY18/Winke_Paula/18-009/SAWpaper
#> +-- data
#> |   +-- DF_CORR.csv
#> |   +-- DF_CRM.csv
#> |   \-- SAW_Paper_Data.RData
#> +-- DESCRIPTION
#> +-- inst
#> |   +-- Development_Tools.R
#> |   +-- extdata
#> |   |   +-- df_corr.sav
#> |   |   \-- df_crm.sav
#> |   +-- R_Citations.Rmd
#> |   +-- SAW_Paper_Import_Data.pdf
#> |   +-- SAW_Paper_Import_Data.Rmd
#> |   +-- SAW_Paper_Spanish_Analysis.pdf
#> |   \-- SAW_Paper_Spanish_Analysis.Rmd
#> +-- LICENSE
#> +-- man
#> |   \-- SAWpaper-package.Rd
#> +-- NAMESPACE
#> +-- NEWS.md
#> +-- R
#> |   \-- SAWpaper-package.R
#> +-- README.md
#> +-- README.Rmd
#> \-- SAWpaper.Rproj
```

We are aiming for a folder structure that fully complies with the R
package structure conventions used on
[CRAN](https://cran.r-project.org/) and discussed in Wickham and Bryan
(2020, <https://r-pkgs.org>). Those prescribe certain folder names,
paths, and contents.

-   The `SAWpaper` folder holds some files required for an R package,
    plus a set of subfolders.
-   The `data` subfolder holds only .RData and .Rds files
    (<https://r-pkgs.org/data.html>) created by our scripts. It will be
    empty when you first copy the repository to your computer.
-   The `inst` subfolder is where we store our R Markdown (.Rmd) scripts
    for data management and analysis, associated PDF output files, and
    other files.
-   The `inst/extdata` subfolder is where our scripts will look for
    external data files that are not stored in either .RData or .Rds
    file formats (<https://r-pkgs.org/data.html>). Thus, this is where
    you would need to put the raw data files.
-   The `man` folder stores R help files associated with the package.
    These are generally updated by processes used when building the
    package such as running `devtools::document()` and
    `devtools::check()`. Those commands read files from the roxygen
    comments in files stored in `SAWpaper/R` and extract the help
    documentation.
-   The `R` folder normally holds R scripts (.R files) used to define
    the custom functions developed for and used in the package. These
    scripts should contain comments formatted for use by the *roxygen2*
    package that are used to automate building the help files for the
    package and its custom functions. *SAWpaper* does not yet contain
    any custom functions (those got moved over to *piercer*).

This repository contains data files, the R markdown scripts used to
analyze them, plus the output from when we ran the scripts. There is
considerably more raw statistical output than we could put directly into
the resulting manuscript. That is preserved here for the sake of
reproducibility and completeness of reporting. We also include other
files necessary to work with the repository in RStudio and GitHub and to
build the R package from the repository files.

To reproduce our results, use RStudio to open the RStudio project file
called `SAWpaper/SAWpaper.proj`, which should be in the local repository
folder on your computer. Then, use RStudio to open and knit the
following files in this order.

-   `SAWpaper/inst/SAW_Paper_Import_Data.Rmd`
-   `SAWpaper/inst/SAW_Paper_Spanish_Analysis.Rmd`
-   `SAWpaper/inst/R_Citations.Rmd`

## Obtaining Data Files

The data files required to use this package are not available in the
GitHub repository. We plan to deposit them with the [Inter-university
Consortium for Political and Social
Research](https://www.icpsr.umich.edu/). Once we have done so, we will
update this section with the reference and a link to the deposited
materials. After you get the files, put them all in the subfolder called
`SAWpaper/inst/extdata`.

## Data File Documentation

There are some data files included in this repository. The are located
in the *data* folder and stored as comma separated values in text files
(i.e., .csv files). We briefly describe the contents of each file below.

``` r
# Load some useful packages.
library(here)
library(knitr)

# Read in the included data files. 
df_corr <- read.csv(here::here("data/DF_CORR.csv"))
df_crm  <- read.csv(here::here("data/DF_CRM.csv"))
```

### Learner Data File: *data/DF_CORR.csv*

This data file has one row per Spanish language learner in our study,
with *N* = 807 observations and 63 variables. The first few rows of data
are shown below.

``` r
# Display top few rows of df_corr.
kable(head(df_corr))
```

|   X | student_id | Gender | Course | OPIc | OPIC | Level | Item1 | Item2 | Item3 | Item4 | Item5 | Item6 | Item7 | Item8 | Item9 | Item10 | Item11 | Item12 | Item13 | Item14 | Item15 | Item16 | Item17 | Item18 | Item19 | Item20 | Item21 | Item22 | Item23 | Item24 | Item25 | Item26 | Item27 | Item28 | Item29 | Item30 | Item31 | Item32 | Item33 | Item34 | Item35 | Item36 | Item37 | Item38 | Item39 | Item40 | Item41 | Item42 | Item43 | Item44 | Item45 | Item46 | Item47 | Item48 | Item49 | Item50 | Item1_10 | Item11_20 | Item21_30 | Item31_40 | Item41_50 | Item1_50 |
|----:|:-----------|:-------|-------:|:-----|-----:|------:|------:|------:|------:|------:|------:|------:|------:|------:|------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|---------:|----------:|----------:|----------:|----------:|---------:|
|   1 | A12479352  | Female |    100 | NL   |    1 |     1 |     1 |     2 |     1 |     1 |     3 |     1 |     2 |     2 |     1 |      1 |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |       15 |        NA |        NA |        NA |        NA |       15 |
|   2 | A12658221  | Male   |    200 | IL   |    4 |     1 |     3 |     4 |     4 |     4 |     3 |     3 |     3 |     3 |     3 |      3 |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |       33 |        NA |        NA |        NA |        NA |       33 |
|   3 | A12711564  | Female |    200 | IL   |    4 |     2 |     4 |     4 |     4 |     4 |     4 |     4 |     4 |     4 |     4 |      3 |      3 |      4 |      4 |      4 |      3 |      3 |      3 |      3 |      4 |      3 |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |       39 |        34 |        NA |        NA |        NA |       73 |
|   4 | A12879916  | Female |    200 | IM   |    5 |     5 |     4 |     4 |     3 |     4 |     4 |     4 |     4 |     4 |     4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      3 |      4 |      4 |      4 |      4 |      4 |      4 |      3 |      4 |      4 |      3 |      4 |      4 |      3 |      4 |      3 |      4 |      4 |      3 |      3 |      4 |      3 |      3 |       39 |        40 |        39 |        38 |        34 |      190 |
|   5 | A13226298  | Male   |    200 | NH   |    3 |     1 |     3 |     4 |     3 |     2 |     2 |     3 |     3 |     2 |     2 |      2 |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |       26 |        NA |        NA |        NA |        NA |       26 |
|   6 | A13320012  | Female |    200 | NM   |    2 |     1 |     3 |     3 |     4 |     4 |     3 |     3 |     3 |     3 |     2 |      3 |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |       31 |        NA |        NA |        NA |        NA |       31 |

This is the data file to use when examining simple correlations between
variables like OPIC and Course. The variables are described below.
Remember that R is case-sensitive with variable names, so OPIc and OPIC
are different (but related) variables.

-   *id*: An anonymized participant identification number. Each learner
    has a unique id value. The values are integer numbers.

-   *Course*: The level of the Spanish language course the learner was
    taking at the time of taking the self-assessment test. First year
    courses are coded 100, second year courses are coded 200, third year
    courses are coded 300, and fourth year courses are coded 400. Course
    values are stored as integers.

-   *OPIc*: These two-character alphabetic codes are values for scores
    on the American Council on the Teaching of Foreign Languages (ACTFL)
    Oral Proficiency Interview - Computer (OPIc) test for Spanish
    language proficiency. The possible scores, in increasing level of
    proficiency, are:

    -   *NL*: Novice low.
    -   *NM*: Novice mid.
    -   *NH*: Novice high.
    -   *IL*: Intermediate low.
    -   *IM*: Intermediate mid.
    -   *IH*: Intermediate high.
    -   *AL*: Advanced low.
    -   *AM*: Advanced mid.
    -   *AH*: Advanced high.
    -   *S*: Superior (which does not occur in thie dataset).

-   *OPIC*: These integer values are a simple recode of the OPIc
    variable. The possible scores, in increasing level of proficiency,
    are:

    -   *1*: Novice low.
    -   *2*: Novice mid.
    -   *3*: Novice high.
    -   *4*: Intermediate low.
    -   *5*: Intermediate mid.
    -   *6*: Intermediate high.
    -   *7*: Advanced low.
    -   *8*: Advanced mid.
    -   *9*: Advanced high.
    -   *10*: Superior (which does not occur in thie dataset).

-   *Level*: These integer values show the maximum level the learner
    reached on the self-assessment test based on 50 Can-Do statements.
    There are five possible levels (1 through 5), with higher values
    indicating greater self-assessed proficiency.

### Level-Transition Test Data File: *data/DF_CRM.csv*

This data file has one row per level transition test attempted by a
learner in our study, with *N* = 1320 observations and 66 variables. The
first few rows of data are shown below.

``` r
# Display top few rows of df_crm.
kable(head(df_crm))
```

|   X | student_id | Gender | Course | OPIc | OPIC | COPIC | Level | pass | Item1 | Item2 | Item3 | Item4 | Item5 | Item6 | Item7 | Item8 | Item9 | Item10 | Item11 | Item12 | Item13 | Item14 | Item15 | Item16 | Item17 | Item18 | Item19 | Item20 | Item21 | Item22 | Item23 | Item24 | Item25 | Item26 | Item27 | Item28 | Item29 | Item30 | Item31 | Item32 | Item33 | Item34 | Item35 | Item36 | Item37 | Item38 | Item39 | Item40 | Item41 | Item42 | Item43 | Item44 | Item45 | Item46 | Item47 | Item48 | Item49 | Item50 | Item1_10 | Item11_20 | Item21_30 | Item31_40 | Item41_50 | Item1_50 | Highest_level |
|----:|:-----------|:-------|-------:|:-----|-----:|------:|------:|-----:|------:|------:|------:|------:|------:|------:|------:|------:|------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|---------:|----------:|----------:|----------:|----------:|---------:|--------------:|
|   1 | A12479352  | Female |    100 | NL   |    1 |    -4 |     1 |    0 |     1 |     2 |     1 |     1 |     3 |     1 |     2 |     2 |     1 |      1 |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |       15 |        NA |        NA |        NA |        NA |       15 |             1 |
|   2 | A12658221  | Male   |    200 | IL   |    4 |    -1 |     1 |    0 |     3 |     4 |     4 |     4 |     3 |     3 |     3 |     3 |     3 |      3 |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |       33 |        NA |        NA |        NA |        NA |       33 |             1 |
|   3 | A12711564  | Female |    200 | IL   |    4 |    -1 |     1 |    1 |     4 |     4 |     4 |     4 |     4 |     4 |     4 |     4 |     4 |      3 |      3 |      4 |      4 |      4 |      3 |      3 |      3 |      3 |      4 |      3 |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |       39 |        34 |        NA |        NA |        NA |       73 |             2 |
| 810 | A12711564  | Female |    200 | IL   |    4 |    -1 |     2 |    0 |     4 |     4 |     4 |     4 |     4 |     4 |     4 |     4 |     4 |      3 |      3 |      4 |      4 |      4 |      3 |      3 |      3 |      3 |      4 |      3 |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |     NA |       39 |        34 |        NA |        NA |        NA |       73 |             2 |
|   4 | A12879916  | Female |    200 | IM   |    5 |     0 |     1 |    1 |     4 |     4 |     3 |     4 |     4 |     4 |     4 |     4 |     4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      3 |      4 |      4 |      4 |      4 |      4 |      4 |      3 |      4 |      4 |      3 |      4 |      4 |      3 |      4 |      3 |      4 |      4 |      3 |      3 |      4 |      3 |      3 |       39 |        40 |        39 |        38 |        34 |      190 |             5 |
| 811 | A12879916  | Female |    200 | IM   |    5 |     0 |     2 |    1 |     4 |     4 |     3 |     4 |     4 |     4 |     4 |     4 |     4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      4 |      3 |      4 |      4 |      4 |      4 |      4 |      4 |      3 |      4 |      4 |      3 |      4 |      4 |      3 |      4 |      3 |      4 |      4 |      3 |      3 |      4 |      3 |      3 |       39 |        40 |        39 |        38 |        34 |      190 |             5 |

This dataset is used in continuation-ratio modeling of the
self-assessment test results. The data shown above have two rows for id
= 3. They show that this learner passed the level transition test to get
from level 1 to level 2, but failed to pass the transition test to get
from level 2 to level 3. The variables are described in more detail
below.

-   *id*: An anonymized participant identification number. Each learner
    has a unique id value. The values are integer numbers.

-   *Course*: The level of the Spanish language course the learner was
    taking at the time of taking the self-assessment test. First year
    courses are coded 100, second year courses are coded 200, third year
    courses are coded 300, and fourth year courses are coded 400. Course
    values are stored as integers.

-   *COPIC*: These integer values are a centered version of the OPIC
    variable found in *df_corr*. We centered around Intermediate-mid
    (OPIC = 5) because it is the level of proficiency expected of
    students exiting the 200-level courses. The centered scores, in
    increasing level of proficiency, are:

    -   *-4*: Novice low.
    -   *-3*: Novice mid.
    -   *-2*: Novice high.
    -   *-1*: Intermediate low.
    -   *0*: Intermediate mid (expected proficiency for students after
        200-level courses).
    -   *1*: Intermediate high.
    -   *2*: Advanced low.
    -   *3*: Advanced mid.
    -   *4*: Advanced high.
    -   *5*: Superior (which does not occur in thie dataset).

-   *Level*: These integer values show which level transition test from
    the Can-Do self-assessment the learner was attempting pass on a
    given row of data. There are four possible level transition tests:

    -   *1*: Transition from level 1 to level 2.
    -   *2*: Transition from level 2 to level 3.
    -   *3*: Transition from level 3 to level 4.
    -   *4*: Transition from level 4 to level 5.

-   *pass*: This binary integer variable is coded 0 when the learner did
    not pass the level transition test shown in the Level variable, and
    1 when the learner pased the test.

# References

Bryan, J. (2018). Excuse me, do you have a moment to talk about version
control? *The American Statistician, 72*(1), 20-27.
[doi:10.1080/00031305.2017.1399928](https://doi.org/10.1080/00031305.2017.1399928)

Bryan, J., & Hester, J. (n.d.). *What they forgot to teach you about R*.
<https://rstats.wtf>

Bryan, J., The STAT 545 TAs, & Hester, J. (n.d.). *Happy Git and GitHub
for the useR*. <https://happygitwithr.com>

Chacon, S., & Straub, B. (2014). *Pro Git* (2nd. ed.) \[PDF file\].
Apress Media. <https://git-scm.com/book/en/v2>

Mair, P. (2016). Thou shalt be reproducible! A technology perspective.
*Frontiers in Psychology, 7*(1079), 1-17.
[doi:10.3389/fpsyg.2016.01079](http://dx.doi.org/10.3389/fpsyg.2016.01079)

Marwick, B., Boettiger, C., & Mullen, L. (2018). Packaging data
analytical work reproducibly using R (and friends). *The American
Statistician, 72*(1), 80-88.
[doi:10.1080/00031305.2017.1375986](https://doi.org/10.1080/00031305.2017.1375986)

Perez-Riverol, Y., Gatto, L., Wang, R., Sachsenberg, T., Uszkoreit, J.,
Leprevost, F. d. V., . . . Vizcaíno, J. A. (2016). Ten simple rules for
taking advantage of Git and GitHub. *PLoS Computational Biology, 12*(7),
e1004947. <https://doi.org/10.1371/journal.pcbi.1004947>

RStudio Team. (2021). RStudio: Integrated development for R (Version
1.4.1717) \[Computer software\]. RStudio, Inc. <https://rstudio.com>

Torvalds, L., Hamano, J. C., & other contributors to the Git Project.
(2021). Git for Windows (Version 2.33.0.2) \[Computer program\].
Software Freedom Conservancy. Retrieved from <https://git-scm.com>

Wickham, H., & Bryan, J. (2021). *R packages: Organize, test, document,
and share your code* (2nd ed.). \[Website, online book in preparation\].
O’Reilly Media. <https://r-pkgs.org>
