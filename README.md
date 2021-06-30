# BECI figs
 Collating data and creating figures on catch and status of important North Pacific fish stocks, in order to support the BECI proposal by the NPAFC for the U.N. Decade of Ocean Science.


## 'data' folder
This folder contains the .csv files that are pulled into the RStudio workspace and analyzed.

### *Important files and folders*
*NPFC_data_READ.ME.txt*: some notes on the abbreviations and data limitations in the NPFC catch and effort data.

*'rawdata'* folder: the raw, unformatted data from the North Pacific Fisheries Commission (NPFC) and the National Ocean and Atmospheric Administration (NOAA)'s 2020 stock assessment of Pacific cod in US waters. the READ.ME.txt has the sources for these files.


## 'scripts' folder
This folder contains the scripts for creating plots for all NPFC catch data ```NPFC catch data.Rmd``` and printing a PDF report on Pacific saury fisheries ```Pacificsauryreport_Jun252021.Rmd```.

## 'output' folder
This folder is where figures and RMarkdown reports write to, given the ```here::here``` function.

### *Important files and folders*
*'figures'* folder: where figures from ```NPFC catch data.Rmd``` write to. The default for separate figures apart from report.

*'reports'* folder: where the RMarkdown knits and exports the PDF to, given a short code snippet at the end:
```{r, echo=FALSE}
rmarkdown::render("C:/Users/Andrew Chin/Documents/GitHub/BECI figs/output/reports/Pacificsauryreport_Jun252021.pdf")
```

*'rmd'* folder: where report figures not generated in R are saved. They are included in the report via their file path, so these must be edited before compiling the report.
