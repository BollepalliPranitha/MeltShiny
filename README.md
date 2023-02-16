# MeltShiny Documentation

## Purpose
The MeltShiny open-source program was designed and implemented to solve the following problem. Researchers are currently using a legacy program called MeltWin to analyze DNA absorbance data. MeltWin was designed over 20 years ago, and as such, requires older windows systems. Furthermore, a lack of source code makes modification impossible. As such there is a need for a newer program that both includes the functions of MeltWin, runs on modern operating systems, introduces newer features, and provides a intuitive user layout, all of which provide researchers with the best possible work flow.

## Research
The aforementioned research is important. Molecules absorb light differently. This property yields data that can mathematically be translated into the strengths of the bonds formed by the strands of DNA or RNA molecules being tested. Knowing the strength is important for determining the shape and stability of the whole molecule. In biological applications, knowing the structure allows for the understanding of function. 

## Introduction to MeltR
MeltShiny's backend functionality relies on another open-source software called MeltR. MeltR is a R package, written by Jacob Sieg-Penn, a chemistry department faculty member at Penn State University. This program is written entirely in R, and possesses many of the same calcuation and fitting abilities as it's predecessar, MeltWin. Specifcally, both MeltR and MeltWin provide easy and consistant fitting of nucleic acid folding data to obtain thermodynamic parameters. However, the features in MeltR are more robust, and require less input from the user. 

## Benefits of MeltShiny
The downside of MeltR is that users must interact with it via the R console, whereas MeltWin has a graphical user interface. The process of typing in commands into the console can be time consuming, tedius, and requires some technical knowledge. MeltShiny eliminates the need for the console, as it provides an intuitive graphical user interface that relies on the robust and reliable calculations of MeltR. MeltShiny's benefits also extend to it's functionality. User's are provided with automated processing of input files, as well as the automated removal of outliers from both the Van't Hoff plot and the results table. 

## MeltShiny Installation Instructions
### Installing R and RStudio
To run MeltShiny you need to download R and RStudio. First go to this website, https://cran.r-project.org/, and follow the instructions for your machine to install R. Next follow this link to download RStudio: https://posit.co/download/rstudio-desktop/. Scroll down to the downloads section and find the RStudio download link needed for your machine.

### Installing R Packages
Next you will need a install few R packages. Open RStudio and in the console at the bottom type the following command, install.packages(c('devtools','shiny', 'dplyr', 'ggplot2', 'glue', 'methods', 'ggrepel','tidyverse')). The installation of MeltR requires a seperate command, devtools::install_github("JPSieg/MeltR").

### Issues With Installing the Packages?
If you are having issues installing MeltR on your computer, the MeltR repository states you may need to run R as an administrator for installing devtools and MeltR on on Windows. On Mac, you may need to install the Xcode toolbox from the app store to install devtools.

### Installing MeltShiny
Finally, it's time to clone the MeltShiny repository. Open either the server or UI files and click Run App in the top right corner of the code view panel. 

### MeltShiny Input Instructions
For now, you can use the following arguments to fill the inputs. Note, there should be no spaces in any of the inputs. Pathlength: 1,1,1,1,1,1,1,1,1,1 Sequence info: RNA, CGAAAGGU, ACCUUUCG and select 260 for wavelength. All other input defualts are fine. Once the inputs are filled, click the browse button to upload the file test.csv. The file is included in the git repo.
