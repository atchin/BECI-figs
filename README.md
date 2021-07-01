# BECI Figures
Collating data and creating figures on catch and status of important North Pacific fish stocks, in order to support the BECI proposal by the NPAFC for the U.N. Decade of Ocean Science.

## Directory of Relevant Files
*Date suffixes denote the date when significant changes were last made.*

```
IYS_gsi_results_figures
|-- data
|   |-- NPFC_data_READ.ME.txt
|   `-- NPFC_saury_CPUE_2019_stock_assessment_June182021.csv
|   `-- NPFCcatchstats_June102021.csv
|   `-- NPFCeffortstats_June102021.csv
|   `-- pacific_cod_abundance_survey_data_June252021.csv
|   `-- pacific_cod_catch_June252021.csv
|   `-- pacific_cod_catchlimits_June252021.csv
|   `-- raw data
|       |-- NPFC
|       `-- Pacific_cod
|       `-- rawdata_READ.ME.txt
|       `-- USA Fisheries Disasters_Apr20_AS2.xlsx
`-- scripts
|   |-- NPFC catch data.Rmd
|   `-- Pacificsauryreport_June252021.Rmd
`-- output
|   |-- figures
|       |--
|   `-- reports
|   `-- rmd
`-- Literature
`-- NPFC catch data worklog.txt

```

## 'data' folder
This folder contains the .csv files that are pulled into the RStudio workspace and analyzed.

### *Important files and folders*
*NPFC_data_READ.ME.txt*: some notes on the abbreviations and data limitations in the NPFC catch and effort data.

*'rawdata'* folder: the raw, unformatted (*i.e.,* in .xlsx format) data from the North Pacific Fisheries Commission (NPFC) on six priority species, including Pacific saury, and the National Ocean and Atmospheric Administration (NOAA)'s 2020 stock assessment of Pacific cod in US waters.
- [NPFC data (.xlsx format)](https://www.npfc.int/statistics)
- [2020 GOA Pacific cod stock asssessment (PDF report)](https://www.fisheries.noaa.gov/resource/data/2020-assessment-pacific-cod-stock-gulf-alaska)

The READ.ME.txt also has the sources for these files.


## 'scripts' folder
This folder contains the scripts for creating plots for all NPFC catch data ```NPFC catch data.Rmd``` and printing a PDF report on Pacific saury fisheries ```Pacificsauryreport_Jun252021.Rmd```.

## 'output' folder
This folder is where figures and RMarkdown reports write to, given the ```here::here``` function.

### *Important files and folders*
*'figures'* folder: where figures from ```NPFC catch data.Rmd``` write to. The default for separate figures apart from report.

*'reports'* folder: where the RMarkdown knits and exports the PDF to, given a short code snippet at the end of the report:
```{r, echo=FALSE}
rmarkdown::render("C:~/GitHub/BECI figs/output/reports/Pacificsauryreport_Jun252021.pdf")
```

*'rmd'* folder: where report figures not generated in R are stored. They are included in the report via their file path, so these must be edited to your own directory before compiling the report.
