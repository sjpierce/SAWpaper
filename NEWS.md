# SAWpaper 1.0.1, 2022-03-27
* Obtained DOIs from Zenodo.
    * DOI: 10.5281/zenodo.6388010 always points to the latest version. 
    * DOI: 10.5281/zenodo.6388011 specifically points to v1.0.0
* Updated `README.Rmd` and `README.md`
    * Added DOI badge. 
    * Added DOI link to Citing This Package section. 

# SAWpaper 1.0.0, 2022-03-27
* Added final output files produced from running code after installing version 
  1.0.0 on my computer. These correspond to output we used in the manuscript and
  are being bundled into the version 1.0.0 release. 
    * `inst\SAW_Paper_Analyze_Published.pdf`
    * `inst\SAW_Paper_Import_Explore_Published.pdf`
    * `inst\R_Citations_Published.pdf`

# SAWpaper 0.21.0, 2022-03-27
* Updated `.gitignore` to:
    * Omit specific data files instead of entire folders. 
    * Omit selected PDF files and allow others.
* Updated `.Rbuildignore` to:
    * Omit specific data files instead of entire folders. 
    * Omit PDF files.
* Added files:
    * `data\Placeholder.txt`
    * `inst\extdata\Placeholder.txt`

# SAWpaper 0.20.0, 2022-03-26
* Updated software license by updating /adding the files:
    * `DESCRIPTION`
    * `LICENSE`
    * `LICENSE.md`
    * `LICENSE.note`
* Added PNG files used in manuscript.
    * `inst/F4.png`
    * `inst/F5.png`
* Updated `inst/SAW_Paper_Import_Explore_Data.Rmd` to:
    * Fix code alignment. 
    * Updated Software Information section.
* Updated `inst/SAW_Paper_Analyze_Data.Rmd` to: 
    * Improve display of influential cases.
    * Improved captions for index plots of leverage and Cook's D, then removed
      code the generated redundant output.
    * Improved explanatory text and headings.
    * Set chunk options to suppress certain messages.
    * Improved table captions and figure labeling.
    * Updated Software Information section.
    * Removed code that created redundant output. 
    * Stop loading pander package because we no longer need it.
* Updated `inst/R_Citations.Rmd` to:
    * Parameterize the left footer. 
    * Update packages loaded and cited. 
    * Remove Project Information section.
* Updated `README.Rmd` and `README.md` extensively. 

# SAWpaper 0.19.0, 2022-03-25
* Updated `inst/SAW_Paper_Analyze_Data.Rmd` to: 
    * Improved diagnostics plots and figure referencing. 
    * Improve object names for conditional and unconditional pass rates.
    * Improve figures showing main effects and interaction effect. 
    * Improve presentation of AUC results. 
    * Fixed chunk names and associated table reference.
    * Improve object names and eliminate saving unnecessary objects.
    * Add more dynamic table referencing.
    * Remove redundant table. 
    * Remove Remaining Tasks section. 
    * Set chunk options to suppress certain messages.
    * Capitalized references to specific models. 
    * Improved explantory text. 
    * Improve section headings and prevent tables/figures from floating beyond
      their section.
    * Fix warning message from residual plots.
    * Fixed contrast labelling and signs of selected comparisons for Model 2b 
      nd improved object names.

# SAWpaper 0.18.0, 2022-03-24
* Updated `README.Rmd` and `README.md` to:
    * Updated introduction paragraph.
    * Update Obtaining Data Files section.
    * Remove Associated Research Paper section. 
    * Updated References section.
* Updated `inst/SAW_Paper_Import_Explore_Data.Rmd` to:
    * Read in final archived data files. 
    * Add reference for the archived data files. 
* Updated `inst/SAW_Paper_Analyze_Data.Rmd` to: 
    * Add reference for the archived data files. 
    * Improve calibration plots and summaries of Hosmer-Lemeshow tests. 
    * Save predicted values for all models in one step.
    * Convert classification measures to tables.
    * Improve object names in the Correlations section.

# SAWpaper 0.17.0, 2022-03-18
* Updated `inst/SAW_Paper_Analyze_Data.Rmd` to: 
    * Collect descriptions of statistical methods and model diagnostics together 
      in one place to reduce redundancy and shorten the document. 
    * Improve headings.
    * Add footnote to regression models table.
    * Split code into more chunks and add chunk names.
    * Add more dynamic table and figure referencing. 
    * Fix typos. 

# SAWpaper 0.16.0, 2022-03-15
* Updated `inst/SAW_Paper_Analyze_Data.Rmd` to: 
    * Improved AUC plots and figure referencing. 
    * Stopped echoing code for show-models chunk.
    * Improved table formatting. 
    * Delete redundant text and output.
    * Improve figures exported for manuscript. 
    * Fix spelling.

# SAWpaper 0.15.0, 2022-03-14
* Updated `inst/SAW_Paper_Analyze_Data.Rmd` to: 
    * Simplify code for getting and referencing tables of model coefficients 
      with s-values, BFB, and PPH1 statistics. 
    * Fix spelling. 
    * Improve calibration plots and figure referencing.

# SAWpaper 0.14.0, 2022-03-13
* Updated `inst/SAW_Paper_Analyze_Data.Rmd` to: 
    * Update comments about loaded packages. 
    * Updated headings.
    * Add more fit statistics to table of regression models (Brier scores, 
      pseudo-R^2, R^2_Dev).
    * Move discussion of Brier scores, pseudo-R^2, and R^_Dev. Reduce 
      commentary on them in the model-specific sections.
    * Update classification code to use revised data frame and variable. 
    * Fixed figure referencing. 
* Updated `DESCRIPTION` to add Depends field. 
* Updated `README.Rmd` and `README.md`.
    * SAWpaper now depends on piercer version 0.11.0 or later.

# SAWpaper 0.13.0, 2022-03-11
* Updated `inst/SAW_Paper_Analyze_Data.Rmd` to: 
    * Improve plot labeling and appearance, plus add figure captions. 
    * Updated variable names in code to match naming in updated data.
    * Load the broom package to simplify some code later. 
    * Suppress hetcor() warnings in output (they are mentioned in the code 
      comments). 
    * Split code into multiple chunks.
    * Add dynamic table referencing in the text and improve table appearance.
    * Set number of digits in regression models table to match what we report 
      in manuscript.
    * Add dynamic table referencing and use pipes to simplify getting tables.
    * Add chunk names.
    
# SAWpaper 0.12.0, 2022-03-07
* Updated `inst/SAW_Paper_Analyze_Data.Rmd` to: 
    * Updated Data Visualization section to use new data frame and variable 
      names, add subheadings, update chunk names, improve explanatory text, and 
      present figures in a better order.
    * Updated Correlations section to use new data and improve text. 

# SAWpaper 0.11.0, 2022-03-06
* Updated `inst/SAW_Paper_Import_Explore_Data.Rmd` to: 
    * Simplify Setup section.
* Updated `inst/SAW_Paper_Analyze_Data.Rmd` to: 
    * Reformat line breaks for readability. 
    * Reformat References in APA 7th Ed. style.
    * Updated explanation of data read in and added a table summarizing data 
      frame sizes. 
    * Simplify Setup section.
    * Deleted code for output that is already provided in the data import script. 
    * Improved Data Structure Comments section.

# SAWpaper 0.10.0, 2022-03-02
* Updated `inst/SAW_Paper_Import_Explore_Data.Rmd` to: 
    * Improve Software Information section.
    * Updated References section.
    * Update left header. 
    * Improve explanatory text.
* Updated `inst/SAW_Paper_Analyze_Data.Rmd` to: 
    * Improve Software Information section.
    * Updated References section.
    * Improve explanatory text.
* Updated `README.Rmd` and `README.Rmd` to:
    * Add title and authors. 
    * Update task list.
    * Update paper citation and references.
    * Improve explanatory text. 
    * Remove data documentation that will be archived separately.
    * Updated folder tree diagram. 
    * Improved heading structure.
* Removed outdated data files. We now read in from SPSS data files that will be
  be archived separately. 
    * `data/DF_CORR.csv`
    * `data/DF_CRM.csv`

# SAWpaper 0.9.0, 2022-02-27
* We still need to finish final cleanup. The package is not ready for publishing
  yet because we need to finish the process of splitting the analyses into 
  multiple scripts. 
* Updated SPSS data files to improve metadata and include additional variables. 
    * `inst/extdata/Students_Data.sav` 
    * `inst/extdata/Testlet_Attempts_Data.sav`
* Updated `inst/SAW_Paper_Import_Explore_Data.Rmd` to: 
    * Use the updated data files.
    * Improve explanatory text. 
    * Improve table showing OPIC variable coding and frequency. 
    * Split exploration of student data into sections for all students versus 
      the subset of students with valid OPIC scores. 
    * Improve table captions and footnotes.
    * Update exploration of testlet-level data to focus on data from students 
      with valid OPIC scores.
    * Update paper citation. 
    * Update data saaved out. 

# SAWpaper 0.8.0, 2022-02-06
* We have resubmitted the manuscript and expect that it will be accepted this 
  time. Therefore, we are doing final cleanup and formatting to ensure 
  reproducibility of all reported results.
    * Updated SPSS data files to correct one case where the student had actually 
      reached Level 5 (by passing Testlet 4) but had been inaccurately recorded 
      as having only reached Level 4 and not passing Testlet 4). We discovered 
      this while updating data files into more convenient form for archiving at 
      ICPSR. The fixes to the data make no substantive difference in our 
      conclusions, but do change some estimates by a small amount in the 
      decimal places.
        * `inst/extdata/Students.sav` 
        * `inst/extdata/Testlet_Attempts.sav`
    * We need to add tables to one of the scripts to ensure users can reproduce 
      information about students where were excluded from the analysis because
      they got OPIc scores that were above range (AR), below range (BR), or 
      unratable (UR). This was added to the paper to respond to a peer review 
      comment. It will require updating the SPSS data files again too. 
* Updated `DESCRIPTION` to remove Paula Winke as author, per conversation we 
  had after I had added her. 
* Updated `inst/SAW_Paper_Analyze_Data.Rmd`: 
    * Updated Correlations section to use additional variables and reflect 
      updated input data frame. 
    * We still have to revise this script further to simplify and prepare for 
      publishing the research compendium. 

# SAWpaper 0.7.1, 2022-01-06
* Updated `DESCRIPTION` to add Paula Winke as author. 

# SAWpaper 0.7.0, 2021-12-04
* Renamed `inst/SAW_Paper_Spanish_Analysis.Rmd` to 
  `inst/SAW_Paper_Analyze_Data.Rmd`.
* Updated `inst/SAW_Paper_Analyze_Data.Rmd`.
    * Updated title & left header. 
    * Improve Software Information section.
    * Load additional package. 
    * Updated citation for the manuscript.
    * Updated Target Journal section. 
    * Improve heading structure.
    * Improve Setup section.
    * Improve Load Data section.
    * Delete content that is now in `inst/SAW_Paper_Import_Explore_Data.Rmd`. 
    * Renamed data frames to match revised data being loaded. 
    * Renamed code chunks.
    * Split figures into separate chunks. 
    * Improve figure referencing. 
    
# SAWpaper 0.6.0, 2021-12-04
* Renamed external data files to clarify what kind of data they contain. 
    * `inst/extdata/df_corr.sav` to `inst/extdata/Students.sav`. 
    * `inst/extdata/df_crm.sav` to `inst/extdata/Testlet_Attempts.sav`. 
* Renamed `inst/SAW_Paper_Import_Data.Rmd` to 
  `inst/SAW_Paper_Import_Explore_Data.Rmd`.
* Updated `inst/SAW_Paper_Import_Explore_Data.Rmd`.
    * Fix filename in here::i_am() call. 
    * Renamed data frames read in from external data files. 
    * Improved heading structure and added/improved explanatory text.
    * Format object names used in explanatory text. 
    * Improve table captions, construction, formatting, and footnotes. 
    * Update in-text citation for the manuscript. 
    
# SAWpaper 0.5.1, 2021-12-03
* Updated `inst/SAW_Paper_Import_Data.Rmd`. 
    * Search & replace word "learner" with "student" for consistency.
    * Load SAWpaper package. 
    * Ensure tables will repeat headers if they break across pages.
    * Improve heading structure and ensure tables stay in their own sections. 
    * Improve table designs. 

# SAWpaper 0.5.0, 2021-12-03
* Updated `inst/SAW_Paper_Import_Data.Rmd`. 
    * Converted some chunk output for contrast coding to tables. 
    * Improved explanatory text. 
    * Added a table showing relation of OPICN an COPIC variables. 

# SAWpaper 0.4.0, 2021-11-07
* Updated `.gitignore` to stop tracking data files. 
* Updated `README.Rmd` and `README.md` files to:
   * Mention a new script. 
   * Fix a chunk name. 
* Added `inst/SAW_Paper_Import_Data.Rmd`. 
* Updated `inst/SAW_Paper_Spanish_Analysis.Rmd` to:
   * Change how we load data files. 
   * Improve explanatory text. 

# SAWpaper 0.3.9, 2021-09-26
* Updated `README.Rmd` and `README.md` files to:
   * Add a chunk name for global-options chunk.
   * Load some packages. 
   * Add a Disclaimer section. 
   * Improve the Software Environment section.
   * Improve the Installation section. 
   * Improve the Repository Contents section.
   * Add the Obtaining Data Files section.
   * Update References section. 
   * Update the Task List section. 
* Updated `inst/SAW_Paper_Spanish_Analysis.Rmd` to fix alignment of a comment. 

# SAWpaper 0.3.8, 2021-09-19
* We are using R 4.1.1 now. 
* Updated `DESCRIPTION` to:
    * Correct the department name in the description field. 
    * Update Paula Winke's title. 
    * Update the Roxygen version number. 
* Updated `man/SAWpaper-package.Rd` to:
    * Correct the department name in the description field. 
    * Update Paula Winke's title. 
* Updated `README.Rmd` and `README.md` files to:
    * Correct the department name in the introductory text. 
    * Update Paula Winke's title. 
    * Update the citation for the manuscript. 
    * Update the citations for the funding sources. 
    * Simplify paths to data files. ♦
    * Updated reference for Git software. 
    * Updated Software Environment section.
    * Remove duplicate words. 
* Updated `inst/SAW_Paper_Spanish_Analysis.Rmd` to:
    * Simplify paths to data files. 
    * Removed Document Infomation section. 
    * Removed Funding Sources section to shorten output file. This topic is 
      covered in `README.Rmd` and `README.md` anyway. 
    * Updated Software Information section. 
    * Fix spelling errors.
    * Updated explanatory text and code comments about piercer package. 
    * Load additioal packages. 
* Added `inst/R_Citations.Rmd` script. 
    
# SAWpaper 0.3.7, 2021-09-03
* Updated `DESCRIPTION` to:
    * Fix the authors field. 
    * Update the Roxygen version number. 

# SAWpaper 0.3.6, 2020-05-07
* We are now using R 4.0.0 and piercer 4.0.0.
* Updated `inst/SAW_Paper_Spanish_Analysis.Rmd` to:
    * Improve correlation & crosstab tables. 
    * Fix typos.
    * Load another R package (stringr).

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
