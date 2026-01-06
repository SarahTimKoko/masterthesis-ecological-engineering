# Master Thesis - Nachhaltige Bauplanung im öffentlichen Raum: Lifecycle-Management von Schwammstadt-Komponenten im Projekt Viererfeld/Mittelfeld Bern

Author: Sarah Pfeiffer

Institution: ZHAW, Institute of Natural Resource Sciences (IUNR)

Date: January 2026

The results of this project is automatically deployed to: <https://sarahtimkoko.github.io/masterthesis-ecological-engineering>


## Description

This repository contains the source code, data analysis, and documentation for my Master Thesis. The project applies Multi-Criteria Analysis (MCA) and Lifecycle Management strategies to optimize "Sponge City" (Schwammstadt) components—specifically trees and surface materials—in coordination with underground infrastructure (pipes and utilities) for the urban development project Viererfeld/Mittelfeld in Bern.

Key Research Goals:

Evaluating tree species and paving materials using MCA to identify optimal solutions.

Modeling maintenance cycles for surfaces and utility lines (sewer, water, electricity) over 100 years.

Optimizing synchronization between surface components and subsurface infrastructure to minimize construction conflicts and excavations.

## Project Structure

The project uses Quarto for literate programming and reproducible research.

-   `R/` - R scripts
-   `data/raw` - raw data
-   `data/tidy` - clean data
-   `output/` - figures, tables, results
-   `\_site/` - generated html site
-   `\_site.yml` - R Markdown site configuration
-   `renv.lock` - environment lock file


├── 00_data_raw
│   ├── Belaege_Gewichtung_Szenario0.xlsx
│   ├── Belaege_Gewichtung_Szenario1.xlsx
│   ├── Belaege_Gewichtung_Szenario2.xlsx
│   ├── Belaege_Gewichtung_Szenario3.xlsx
│   ├── Graben_Matrix.xlsx
│   ├── Kostenzusammenstellung_Beläge.xlsx
│   ├── Leitungen_IST.csv
│   ├── Leitungen_IST.xlsx
│   ├── Rohdaten_Matrix_Baeume.xlsx
│   ├── Rohdaten_Matrix_Baeume_aufgeteilt.xlsx
│   ├── Rohdaten_Matrix_Belaege.xlsx
│   ├── Rohdaten_Matrix_Belaege_aufgeteilt.xlsx
│   ├── Rohdaten_Matrix_Leitungen.csv
│   ├── Rohdaten_Matrix_Leitungen.xlsx
│   ├── Rohdaten_Matrix_Standort_1.csv
│   ├── Rohdaten_Matrix_Standort_1.xlsx
│   ├── Zonen_Tabelle.xlsx
│   └── Übersicht_Bewertungskriterien.xlsx
├── 01_data_input
│   ├── Baeume_Gewichtung_Szenario0.csv
│   ├── Baeume_Gewichtung_Szenario1.csv
│   ├── Baeume_Gewichtung_Szenario2.csv
│   ├── Baeume_Gewichtung_Szenario3.csv
│   ├── Baeume_tidy.csv
│   ├── Belaege_Gewichtung_Szenario0.csv
│   ├── Belaege_Gewichtung_Szenario1.csv
│   ├── Belaege_Gewichtung_Szenario2.csv
│   ├── Belaege_Gewichtung_Szenario3.csv
│   ├── Belaege_tidy.csv
│   └── Leitungen_IST.csv
├── 02_export
│   ├── plots
│   └── tables
├── diagram.qmd
├── images
│   └── titelbild.jpg
├── index.qmd
├── LICENSE
├── MCA_Baeume_Szenario_0_bis_3.qmd
├── MCA_Belaege_Szenario_0_bis_3.qmd
├── R
│   └── utils.R
├── README.md
├── renv
│   ├── activate.R
│   ├── library
│   ├── settings.json
│   └── staging
├── renv.lock
├── R_Project.Rproj
├── Zeitstrahl_Analyse.qmd
├── _archiv
│   ├── Begründung_Gewichtung_Belaege.xlsx
│   ├── Belaege_norm.csv
│   ├── Bewertungsraster.qmd
│   ├── export
│   ├── Gewichtung_Baeume.csv
│   ├── Gewichtung_Baeume.xlsx
│   ├── Gewichtung_Belaege.csv
│   ├── Gewichtung_Belaege.xlsx
│   ├── Gewichtung_Leitungen.csv
│   ├── Gewichtung_Leitungen.xlsx
│   ├── lifecycle_scenarios.qmd
│   ├── lifecycle_scenarios_2.qmd
│   ├── lifecycle_scenarios_3.qmd
│   ├── MCA Belaege Szenario 1 bis 3.qmd
│   ├── MCA.qmd
│   ├── MCA_Belaege_Szenario1.qmd
│   ├── Rohdaten_Matrix_Belaege.csv
│   ├── Viererfeld_Bewertung_MASTER.xlsx
│   ├── Viererfeld_Bewertung_Template.xlsx
│   ├── Viererfeld_Bewertung_Template_2.xlsx
│   └── Viererfeld_Bewertung_Template_weight_Scores.xlsx
├── _freeze
│   ├── diagram
│   ├── MCA Belaege Szenario 1 bis 3
│   ├── MCA Belaege Szenario_0_bis_3
│   ├── MCA_Baeume_Szenario_0_bis_3
│   ├── MCA_Belaege_Szenario1
│   ├── MCA_Belaege_Szenario_0_bis_3
│   ├── site_libs
│   └── Zeitstrahl_Analyse
├── _quarto.yml
└── _site
    ├── 01_data_input
    ├── 02_export
    ├── diagram.html
    ├── images
    ├── index.html
    ├── MCA Belaege Szenario 1 bis 3.html
    ├── MCA Belaege Szenario_0_bis_3.html
    ├── MCA-Belaege-Szenario-1-bis-3_files
    ├── MCA-Belaege-Szenario_0_bis_3_files
    ├── MCA_Baeume_Szenario_0_bis_3.html
    ├── MCA_Baeume_Szenario_0_bis_3_files
    ├── MCA_Belaege_Szenario1.html
    ├── MCA_Belaege_Szenario1_files
    ├── MCA_Belaege_Szenario_0_bis_3.html
    ├── MCA_Belaege_Szenario_0_bis_3_files
    ├── search.json
    ├── site_libs
    ├── Zeitstrahl_Analyse.html
    └── Zeitstrahl_Analyse_files

## Installation & Set up

To reproduce the analysis locally, you need R, RStudio, and Quarto installed.

### 1. Clone the Repository

```r
git clone https://github.com/sarahtimkoko/masterthesis-ecological-engineering.git

```
### 2. Restore the R Environment
This project uses renv to manage package versions. Open the project in RStudio and run:


``` r
install.packages("renv")
renv::restore()

```
This will automatically download and install all necessary packages (tidyverse, ggplot2, etc.) in their correct versions.


## Usage

### Rendering the Website locally
You can render the entire thesis website locally to view the results.

**Method 1: Using RStudio**

- Open the project in RStudio.

- Go to the "Build" tab.

- Click "Render Website" (or press Ctrl+Shift+B / Cmd+Shift+B).

**Method 2: Using Command Line (Terminal)**

``` r
# Live preview (auto-updates on save)
quarto preview

# Full build
quarto render

```

Note: 
- `quarto preview` starts a local server with live preview
- `quarto render` builds the site without starting a server
- The rendered site will be in the `_site` directory


## Install new package with renv

```r
renv::install("<package>")
```

After installing the package and checking that your code works, you should call 

```r
renv::snapshot()
``` 
to record the latest package versions in your lockfile. 

## License & Citation
This work is submitted as a Master Thesis at ZHAW. © 2026 Sarah Pfeiffer





