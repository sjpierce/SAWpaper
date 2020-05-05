# SAWpaper 0.3.5, 2020-05-05
* Updated `README.Rmd` and `README.md` files.

# SAWpaper 0.3.4, 2020-04-30
* Updated `DESCRIPTION` file package title by appending "Research Compendium".

# SAWpaper 0.3.3, 2020-04-28
* Updated `inst/SAW_Paper_Spanish_Analysis.Rmd` to:
    * Simplify code for estimating correlations. 
    * Eliminate loess warning messages from visualization graphs. 
    * Improved format for correlation tables. 
* package now relies on piercer v. 0.3.7

# SAWpaper 0.3.2, 2020-04-27
* Updated `inst/SAW_Paper_Spanish_Analysis.Rmd` to estimate polyserial   
  correlations.
  
# SAWpaper 0.3.1, 2020-04-24
* Updated `inst/SAW_Paper_Spanish_Analysis.Rmd` to estimate Pearson and Spearman 
  correlations.
* Package now relies on piercer version 0.3.4

# SAWpaper 0.3.0, 2020-04-22
* Removed `R/flattenCorrMatrix.R` file and flattenCorrMatrix() function because
  updates to piercer pacakge make it unnecessary. 

# SAWpaper 0.2.0, 2020-03-18
* Added flattenCorrMatrix() function and associated draft of help files. 

# SAWpaper 0.1.4, 2020-03-17
* Updated Description text layout in `DESCTIPTION`. 

# SAWpaper 0.1.3, 2020-03-06
* Updated `inst/SAW_Paper_Spanish_Analysis.Rmd` to remove code for setting 
  monofont to Consolas. 

# SAWpaper 0.1.2, 2020-02-18
* Updated `README.Rmd` and `README.md` task list  added headings.
* Edits to practice using Git  GitHub collaboration with co-author.

# SAWpaper 0.1.1, 2020-02-12
* Updated `DESCRIPTION` to list Xiaowan Zhang as an author. 

# SAWpaper 0.1.0, 2020-02-07
* Added `inst/Development_Tools.R` to store example code useful during package
  development and testing. 
* Updated `inst/SAW_Paper_Spanish_Analysis.Rmd` to:
    * Remove horizontal lines between main sections. 
    * Keep tables and figures in their respective sections. 
    * Update software information. 
* Updated to most recent piercer package to fix a bug in lrcm() that affected 
  `inst/SAW_Paper_Spanish_Analysis.Rmd`.
* Updated `README.Rmd` and `README.md` to:
    * Update the task list.
    * Update software information. 

# SAWpaper 0.0.0.9010, 2020-02-04
* Updated data file names read in by `inst/SAW_Paper_Spanish_Analysis.Rmd`. 
* Replaced `data/df_corr.sv` and `data/df_crm.csv` with final versions that 
  match what will appear in the published data archive. 

# SAWpaper 0.0.0.9009,2019-12-13
* Updated YAML headers in `inst/SAW_Paper_Spanish_Analysis.Rmd`. 
  
# SAWpaper 0.0.0.9008, 2019-12-12
* Started using TinyTeX instead of MiKTeX on my laptop. Updated 
  `inst/SAW_Paper_Spanish_Analysis.Rmd` software information to reflect that. 
* Moved software information section below references in 
  `inst/SAW_Paper_Spanish_Analysis.Rmd`. 
* Removed date field from `inst/SAW_Paper_Spanish_Analysis.Rmd` YAML header. 
* Fixed left footer in `inst/SAW_Paper_Spanish_Analysis.Rmd`. 

# SAWpaper 0.0.0.9007, 2019-12-10
* Added package-level documentation ?SAWpaper via usethis::use_package_doc() and
  devtools::document(). 

# SAWpaper 0.0.0.9006, 2019-12-01
* Updated `inst/SAW_Paper_Spanish_Analysis.Rmd`. Simplified some descriptive 
  statistics code. Renamed some objects, added new Table 1, combined tables 
  to make new Table 3, improved table formatting for Tables 1-6. 

# SAWpaper 0.0.0.9005, 2019-11-16
* Updated `inst/SAW_Paper_Spanish_Analysis.Rmd`. Tested combining some tables.  

# SAWpaper 0.0.0.9004, 2019-11-08
* Updated `README.Rmd` with better introduction text and some details about 
  centering OPIC scores. 
* Updated `inst/SAW_Paper_Spanish_Analysis.Rmd`. Solved LaTeX warnings about 
  float position being changed. 

# SAWpaper 0.0.0.9003, 2019-11-07
* Updated `inst/SAW_Paper_Spanish_Analysis.Rmd`. 

# SAWpaper 0.0.0.9002, 2019-11-02
* Updated `inst/SAW_Paper_Spanish_Analysis.Rmd`. 

# SAWpaper 0.0.0.9002, 2019-11-02
* Updated `SAWpaper.Rproj` to build vignettes along with package. 

# SAWpaper 0.0.0.9001, 2019-10-27
* Created the GitHub repository to store this package. 
* Added `.gitignore` file. 
* Added `.Rbuildignore` file. 
* Added `DESCRIPTION` file. 
* Added `README.Rmd` file and updated `README.md` file.
* Added `NEWS.md` file. 
* Added `graphics/CSTATLogoH.png` file. 
* Added `data/DF_CORR.csv` file. 
* Added `data/DF_CRM.csv` file. 
* Added `inst/SAW_Paper_Spanish_Analysis.Rmd` file, then updated it. 
