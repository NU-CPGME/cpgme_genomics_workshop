# CPGME Genome Analysis Workshop

### May 4, 2022

*Egon A. Ozer, MD PhD (<e-ozer@northwestern.edu>)*  

# Microbial Sequence Assembly & Alignment
---

# Section 1 - Last-minute fixes and download example files

## Section 1.1 Hot Fixes

1. Open up your Terminal 
2. Activate the conda environment: 
    
    ```
    conda activate cpgme_workshop
    ```
3. Enter the following command to update your software and add a few missing items:    

    ```
    conda install -y -c conda-forge -c bioconda prokka=1.14.6 snippy=4.6.0 snpEff=4 biopython=1.76 quast
    ```

## Section 1.2 Download data

1. Use this link to download the demo data folder to your computer:

    ### [Download data](https://downgit.github.io/#/home?url=https://github.com/NU-CPGME/cpgme_genomics_workshop/tree/main/demo_data) 

2. Unzip the folder called **demo_data** and move it somewhere you can find it easily, like your desktop.
3. Navigate your Terminal into the folder either by typing `cd` in your terminal (followed by a space) and dragging the folder icon into the terminal or by typing `cd /path/to/folder` where /path/to/folder is the absolute or relative path to the folder

Ready to go!

---

In the next section we'll take a quick tour of common commands we'll use to navigate around the command line environment: [Basic command line usage](2_command_line.md)

---
<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.