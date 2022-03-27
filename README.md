SAWpaper: Self-Assessment Works Paper Research Compendium
================
Steven J. Pierce & Xiaowan Zhang

<!-- README.md is generated from README.Rmd. Please edit that file -->
<!-- badges: start -->

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.6388011.svg)](https://doi.org/10.5281/zenodo.6388011)
[![Lifecycle:
stable](https://img.shields.io/badge/lifecycle-stable-brightgreen.svg)](https://lifecycle.r-lib.org/articles/stages.html#stable)
[![Project Status:
Inactive](https://www.repostatus.org/badges/latest/inactive.svg)](https://www.repostatus.org/#inactive)
[![CRAN
status](https://www.r-pkg.org/badges/version/cstatops)](https://CRAN.R-project.org/package=SAWpaper)
<!-- badges: end -->

This package and corresponding GitHub repository are intended to enhance
the reproducibility of a research paper (Winke, Zhang, & Pierce, 2022)
by serving as a research compendium (Marwick, Boettiger, & Mullen,
2018). The principal investigators for the study are Dr. Paula Winke
(Professor) and Dr. Susan Gass (University Distinguished Professor),
both of whom belong to the Department of Linguistics, Languages, &
Cultures at Michigan State University. The paper analyzes data on
Spanish language learners who took a Can-Do self-assessment test, along
with the more authoritative OPIc language proficiency test. We did both
correlation analyses and continuation-ratio models that examine the
effect of course and OPIc speaking proficiency scores on the passing
rate for each level of the Can-Do statements self-assessment. The
objective was to validate the Can-Do test results.

# Software Environment

We use R Markdown to enhance reproducibility because it provides
excellent support for generating dynamic reports (Mair, 2016). Knitting
an R Markdown script can generate a PDF output file containing
explanatory text, R code, plus R output (text and graphics), although it
can also produce HTML or Markdown files too depending on the contents of
the R Markdown file. We have designed most of our scripts to produce PDF
output.

-   We used the [R statistical software](https://www.r-project.org/) to
    do data management and run our analyses. You will need R to to
    reproduce our results. We recommend using the most recent stable
    release of R available from the [Comprehensive R Archive Network
    (CRAN)](https://cran.r-project.org/).
-   We used [RStudio](www.rstudio.org) 2022.2.0.443 (RStudio Team, 2021)
    to work with R and R Markdown files. RStudio is an excellent
    integrated development environment (IDE). We recommend using the
    most recent stable release available. The software chain for R
    Markdown looks like this: **Rmd file \> RStudio \> R \> rmarkdown \>
    knitr \> md file \> pandoc \> tex file \> TinyTeX \> PDF file**.
-   A version of [pandoc](https://pandoc.org/) comes bundled with
    RStudio, but if you want the most recent version, download it from
    <https://pandoc.org/>.
-   We use Git (Torvalds et al., 2022) for version control, with the
    primary (i.e., main) repository hosted online by
    [GitHub](https://github.com/). For a short introduction to Git, see
    Bryan (2018). There is a longer, more detailed resource on using Git
    with R at the [Happy Git and GitHub for the
    userR](https://happygitwithr.com) website (Bryan et al., n.d.).
    Other useful resources on using Git and GitHub include Bryan
    2018) and Perez-Riverol et al. (2016). Chacon and Straub (2014) is a
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

# Installation

The *SAWpaper* package is available from a public repository available
on [GitHub](https://github.com/) at
<https://github.com/sjpierce/SAWpaper>. It was made public after the
manuscript was accepted for publication.

## Order of Installation Tasks

Before installing *SAWpaper*, make sure you have:

-   Obtained the *SSACHR* repository from GitHub and reviewed its
    contents.
-   Installed R 4.1.3 or later. You can get the most recent version of R
    from the [Comprehensive R Archive Network
    (CRAN)](https://cran.r-project.org/).
-   Installed any tools required for compiling packages (they will be
    specific to your operating system). These will be necessary for the
    *devtools* package to work. You may find Bryan & Hester’s (n.d.)
    website useful, especially the [Set up an R dev
    environment](https://rstats.wtf/set-up-an-r-dev-environment.html)
    section.
    -   On Windows, see
        <https://cran.r-project.org/bin/windows/Rtools/>.
    -   On Mac OS X, see <https://cran.r-project.org/bin/macosx/tools>
        and <https://mac.R-project.org/tools/>.
-   Installed [TinyTeX](https://yihui.org/tinytex/) or some other
    suitable LaTeX distribution.
-   Installed the [*devtools*](https://devtools.r-lib.org/) package for
    R.
-   Installed the [*piercer*](https://github.com/sjpierce/piercer)
    package for R.
-   Updated your R packages. You may be prompted with a dialog box
    asking “Do you want to install from sources the packages which need
    compilation?” It usually works fine if I choose “no”. Occasionally,
    it appears necessary to choose “yes”, but I am more likely to run
    into problems when doing that.  
-   Install the *SSACHR* package to your R package library.
-   Install additional R packages from CRAN.
-   After installing *SSACHR*, see the Obtaining Data Files section
    below. You will need to download the data from an archive and put
    them in the right subfolder on your computer.

## Obtain the Repository from GitHub

If you use Git (Torvalds et al., 2022) and have a GitHub account, either
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

## Understanding the Repository Structure and Contents

This section reviews the subfolders and files nested under the
`SAWpaper` folder. Our scripts are all designed to use path names
relative to the `SAWpaper` folder, usually by calling the `here::here()`
function, which locates that folder on your computer and fills in the
path up to that point. That increases portability of the repository.

This repository contains the R markdown scripts used to analyze our
data, plus the output from when we ran the scripts. There is
considerably more raw statistical output than we could put directly into
the resulting manuscript. That is preserved here for the sake of
reproducibility and completeness of reporting. We also include other
files necessary to work with the repository in RStudio and GitHub and to
build the R package from the repository files.

The structure for the package is shown in the outline below, where
folder names and file names are `highlighted like this` and comments are
in normal text. We are aiming for a folder structure that fully complies
with the R package structure conventions used on
[CRAN](https://cran.r-project.org/) and discussed in Wickham and Bryan
(2020, <https://r-pkgs.org>). Those prescribe certain folder names,
paths, and contents. The structure deviates a bit from the example
research compendium folder structures discussed by Marwick et
al. (2018). The repository is also set up as an [RStudio
project](https://support.rstudio.com/hc/en-us/articles/200526207-Using-RStudio-Projects).

-   `SAWpaper`: This is the root folder for the repository. It holds
    some files required for an R package, plus a set of subfolders.
    -   `data`: This folder is where the data file produced by the
        script `inst/SAW_Paper_Import_Explore_Data.Rmd` will be stored.
        This is a standard folder for R package structures.
        -   `SAW_Paper_Data.RData` is the data file produced by the
            script `inst/SAW_Paper_Import_Explore_Data.Rmd` after it
            imports the external data files. It is not distributed with
            the repository (see the Obtaining Data Files section).
        -   `Placeholder.text` This text file is just present to ensure
            that the `data` subfolder will be created when you clone the
            repository or extract files from ZIP file copy of the
            repository obtained from GitHub.
    -   `inst`: This folder is where you can find the key files you will
        need to use if you want to re-run our analyses on your own
        computer. The unintuitive name for this folder is a result of R
        package building conventions (it is where you put files that
        should be installed with the package).
        -   `extdata`: This subfolder is where you will need to put the
            SPSS data files mentioned in the Obtaining Data Files
            section below.
            -   `Placeholder.text` This text file is just present to
                ensure that the `inst/extdata` subfolder will be created
                when you clone the repository or extract files from ZIP
                file copy of the repository obtained from GitHub.
        -   `Development_Tools.R`: This file just contains R code
            reminders that I use while developing packages.
        -   `F4.png` is a graphics file created (and overwritten) by
            knitting `SAW_Paper_Analyze_Data.Rmd`.
        -   `F5.png` is a graphics file (and overwritten) by knitting
            `SAW_Paper_Analyze_Data.Rmd`.
        -   `SAW_Paper_Analyze_Data.pdf`: This is the default output
            filename produced by knitting `SAW_Paper_Analyze_Data.Rmd`.
            It is not distributed with the package because you would
            just generate it on your own computer to check
            reproducibility.
        -   `SAW_Paper_Analyze_Data.Rmd`: This file should be knitted
            after you knit `SAW_Paper_Import_Explore_Data.Rmd` because
            it depends on a data files created by that script. It will
            produce a PDF file called `SAW_Paper_Analyze_Data.pdf`.
        -   `SAW_Paper_Analyze_Data_Published.pdf`: This is a copy of
            the final output I produced on my computer when preparing to
            release the package to the public. We relied on it to create
            our manuscript. It is distributed with the package because
            you may want to compare it to the results you get on your
            own computer by knitting `SAW_Paper_Analyze_Data.Rmd`.
        -   `SAW_Paper_Import_Explore_Data.pdf`: This is the default
            output filename produced by knitting
            `SAW_Paper_Import_Explore_Data.Rmd`. It is not distributed
            with the package because you would just generate it on your
            own computer to check reproducibility.
        -   `SAW_Paper_Import_Explore_Data.Rmd`: Knitting this file
            requires that you have already obtained the data files
            mentioned in the Obtaining Data Files section below. It
            performs initial data management steps to prepare the data
            for use in other scripts.
        -   `SAW_Paper_Import_Explore_Data_Published.pdf`: This is a
            copy of the final output I produced on my computer when
            preparing to release the package to the public. We relied on
            it to create our manuscript. It is distributed with the
            package because you may want to compare it to the results
            you get on your own computer by knitting
            `SAW_Paper_Import_Explore_Data.Rmd`.
        -   `R_Citations.pdf`: This is the default output filename
            produced by knitting `R_Citations.Rmd`. It is not
            distributed with the package because you would just generate
            it on your own computer to check reproducibility.
        -   `R_Citations.Rmd`: This file generates details about the R
            packages used by `Step_01_Data_Mgt.Rmd` and
            `Step_02_Analysis.Rmd`. I recommend knitting it after you
            knit those two files. When you knit it, you will get an
            output file called `R_Citations.pdf` showing the citations
            and versions for what is installed and in use on your
            computer.
        -   `R_Citations_Published.pdf`: This is a copy of the final
            output I produced on my computer when preparing to release
            the package to the public. It describes the software
            environment I used to generate the files upon which our
            published manuscript was based. You can compare it to the
            environment on your computer. Maximum reproducibility should
            occur when you are using the environment described in this
            document.
    -   `man`: This folder stores R help files associated with the
        package. These are generally updated by processes used when
        building the package such as running `devtools::document()` and
        `devtools::check()`. Those commands read files from the roxygen
        comments in files stored in `SAWpaper/R` and extract the help
        documentation.
    -   `R`: This folder folder normally holds R scripts (.R files) used
        to define the custom functions developed for and used in the
        package. These scripts should contain comments formatted for use
        by the *roxygen2* package that are used to automate building the
        help files for the package and its custom functions. *SAWpaper*
        does not yet contain any custom functions (those got moved over
        to *piercer*).
        -   `SAWpaper-package.R` This file generates the package-level
            help documentation, which is quite sparse because there are
            no custom functions in this package.
    -   `.gitignore`: This file tells Git what files to ignore and omit
        from synchronizing with the main repository on GitHub.
    -   `.Rbuildignore`: This file tells R what files to ignore when
        building the package from the source code.
    -   `DESCRIPTION`: This file is a brief, structured description of
        the package that is required by R package building conventions.
    -   `LICENSE`: This file contains the terms of the CC-BY-SA-4.0
        license that applies to all non-source code content in this
        repository.
    -   `LICENSE.md`: This file contains the terms of the GPL3 software
        license that apply to the source code in this repository.
    -   `LICENSE.note`: This file contais a notes explaining why there
        are are multiple licenses by specifying which content
        repository/package content falls under each license.
    -   `NAMESPACE`: This file is created automatically by R when
        building the package. You should not edit it manually. It is
        required by R package building conventions.
    -   `NEWS.md`: This file contains an list of comments about the
        changes made with each version of this package. It is required
        by R package building conventions
    -   `README.md`: This file is obtained by knitting the `README.Rmd`
        file and is used by GitHub to display information about the
        package. Do not edit it manually. In R Studio, you can read the
        formatted version by opening the file and clicking the Preview
        button.
    -   `README.Rmd`: This file gives an introduction to the package.
        Knitting it produces the `README.md` file and opens the preview
        automatically.
    -   `SAWpaper.Rproj`: This is an RStudio project file. It contains
        settings for working with the project in that software.

## Install *devtools* from CRAN to Your Package Library

You will need to install the [*devtools*](https://devtools.r-lib.org/)
package before you install *piercer* in the next step. You can find
*devtools* [on CRAN](https://cran.r-project.org/package=devtools) and
[on GitHub](https://github.com/r-lib/devtools). The most recent CRAN
release will likely be more stable but sometimes you may instead need
the development version from GitHub. The code below will allow you to
install the current release version from CRAN.

``` r
install.packages("devtools")
```

## Install *piercer* from GitHub to Your Package Library

Please read and follow the installation instructions for *piercer* at
<https://github.com/sjpierce/piercer> before trying to use this package.
You need version 0.11.0 or higher.

## Install *SAWpaper* from GitHub to Your Package Library

This package doesn’t have any custom functions, so this step mostly just
adds some help system documentation and ensures that the version number
for the package will show up in the output files. Downloading or cloning
the repository files to your computer does not install that package into
your R package library. It just creates your local copy of the
repository files.

To install the package to your R package library, you have to either
build and install the package from those local files, or install it
directly from GitHub.

The following code will install *SAWpaper* directly from the Github
repository into your personal package library by using the
`install_github()` function from *devtools*.

``` r
devtools::install_github("sjpierce/SAWpaper")
```

## Install Additional R Packages from CRAN

Scripts in this R package depend on having a number of other R packages
installed. Those packages are available from CRAN and can be installed
by running the following code in the R console.

``` r
install.packages(pkgs = c("broom", "car", "directlabels", "dplyr", "ggplot2",
                          "haven", "Hmisc", "here", "kableExtra", "knitr",
                          "lattice", "modEVA", "multcomp", "polycor", "pROC",
                          "rmarkdown", "sjlabelled","stringr", "texreg", 
                          "tidyr", "visreg", "xfun"))
```

Once you have completed this step, you should be ready to use this
package to reproduce our results.

# Obtaining Data Files

The data files required to use this package are not available in the
GitHub repository. They were instead deposited with the
[Inter-university Consortium for Political and Social
Research](https://www.icpsr.umich.edu/) as [Winke & Zhang
(2022)](https://doi.org/10.3886/E164981V1). After you get the SPSS data
files, put them all in the subfolder called `SAWpaper/inst/extdata`.

# Loading the *SAWpaper* Package in R

After it has been installed to your package library as described above,
you can load *SAWpaper* via the following R console command. That
provides access to the custom R functions we have included in the
package.

``` r
library(SAWpaper)
```

Loading the package will also mean that we can use functions like
`devtools::session_info()` to show the package version number in our
output. That facilitates reproducibility by making it easier to see the
software environment required to obtain a particular result.

# Get Help on *SAWpaper* Custom Functions

You can see information about the package by using the following command
in the R console. The resulting help page has an Index link at the
bottom that will show you a list of all the custom functions in the
package (currently none).

``` r
?SAWpaper
```

# Reproduce Our Results

If you are using [RStudio
Desktop](https://www.rstudio.com/products/rstudio/), the easiest way to
start reproducing our results is to navigate to the `SAWpaper` folder
containing the repository and open the project file
`SAWpaper\SAWpaper.Rproj`.

Then you can open and knit the key scripts in the following order:

-   `SAWpaper/inst/SAW_Paper_Import_Explore_Data.Rmd`
-   `SAWpaper/inst/SAW_Paper_Analyze_Data.Rmd`
-   `SAWpaper/inst/R_Citations.Rmd`

To do that from the R console, the following code should work. Each call
to `Rscript_call()` runs the listed input script in a fresh R session
and writes a PDF output file to the specified name and folder inside the
local repository. That will replace any prior version of the output by
overwriting the file.

``` r
library(xfun)      # for Rscript_call()
library(here)      # for here()
library(rmarkdown) # for render()
Rscript_call(fun = render,
             args = list(input = here("inst/SAW_Paper_Import_Explore_Data.Rmd"),
                         output_file = "SAW_Paper_Import_Explore_Data.pdf",
                         output_dir = here("inst")))

Rscript_call(fun = render,
             args = list(input = here("inst/SAW_Paper_Analyze_Data.Rmd"),
                         output_file = "SAW_Paper_Analyze_Data.pdf",
                         output_dir = here("inst")))

Rscript_call(fun = render,
             args = list(input = here("inst/R_Citations.Rmd"),
                         output_file = "R_Citations.pdf",
                         output_dir = here("inst")))
```

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

RStudio Team. (2022). RStudio: Integrated development for R (Version
2022.02.0.443) \[Computer software\]. RStudio,
Inc. <https://rstudio.com>

Torvalds, L., Hamano, J. C., & other contributors to the Git Project.
(2022). Git for Windows (Version 2.35.1(2)) \[Computer program\].
Software Freedom Conservancy. Retrieved from <https://git-scm.com>

Wickham, H., & Bryan, J. (2021). *R packages: Organize, test, document,
and share your code* (2nd ed.). \[Website, online book in preparation\].
O’Reilly Media. <https://r-pkgs.org>

Winke, P., & Zhang, X. (2022, March 14). *Data and codebook for SSLA
article: “A closer look at a marginalized test method: Self-assessment
as a measure of speaking proficiency.”* (Study 164981; Version V1)
\[Data files and codebooks\]. Inter-university Consortium for Political
and Social Research. <https://doi.org/10.3886/E164981V1>

Winke, P., Zhang, X., & Pierce, S. J. (2022). A closer look at a
marginalized test method: Self-assessment as a measure of speaking
proficiency \[Manuscript accepted for publication\]. *Studies in Second
Language Acquisition*.

# Funding Support

Funding for this research was provided by the following grants.

Winke, P., Gass, S., & Pierce, S. J. (08/01/2017–12/31/2018). *Michigan
State University Language Flagship Proficiency Initiative Year 4
continuation proposal* (Award \#: 0054-MSU-22-PI-280-PO2) \[Grant\].
Institute of International Education.

Winke, P., Gass, S., & Pierce, S. J. (01/01/2019–12/31/2019). *Michigan
State University Language Flagship Proficiency Initiative Year 5
continuation proposal* (Award \#: 0054-MSU-22-PI-280-PO2) \[Grant\].
Institute of International Education.

# Disclaimer

The opinions or points of view expressed in this research compendium and
the associated manuscript are solely those of the authors and do not
reflect the official positions of any organization or the Institute of
International Education.

# Citing This Package

Please cite the package itself, plus the associated data files and the
journal article.

Pierce, S. J., & Zhang, X. (2022). *SAWpaper: Self-assessment works
paper research compendium*. (Version 1.0.0) \[Reproducible research
materials and computer program, R package\]. GitHub and Zenodo.
<https://github.com/sjpierce/SAWpaper> and
<https://doi.org/10.5281/zenodo.6388011>

Winke, P., & Zhang, X. (2022, March 14). *Data and codebook for SSLA
article: “A closer look at a marginalized test method: Self-assessment
as a measure of speaking proficiency.”* (Study 164981; Version V1)
\[Data files and codebooks\]. Inter-university Consortium for Political
and Social Research. <https://doi.org/10.3886/E164981V1>

Winke, P., Zhang, X., & Pierce, S. J. (2022). A closer look at a
marginalized test method: Self-assessment as a measure of speaking
proficiency \[Manuscript accepted for publication\]. *Studies in Second
Language Acquisition*.
