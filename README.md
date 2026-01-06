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

-   `.github/workflows/render-and-deploy.yaml` - GitHub Action to render and deploy the Quarto site
-   `00_data_raw` - raw data
-   `01_data_input` - generated tidy data based on `00_data_raw`
-   `02_export/plots` - figures, plots, results
-   `02_export/tables` - tables, results
-   `images` - images for the rendered quarto site
-   `renv` - configuration for `renv` dependency management
-   `renv.lock` - environment lock file
-   `_quarto.yml` - Quarto site configuration
-   `index.qmd` - Quarto site index
-   `MCA_Belaege_Szenario_0_bis_3.qmd` - Quarto site and code MCA Belaege
-   `MCA_Baeume_Szenario_0_bis_3.qmd` - Quarto site and code MCA Baeume
-   `Zeitstrahl_Analyse.qmd` - Quarto site and code Zeitstrahl Analyse
-   `R_Project.Rproj`- project file for RStudio

## Installation & Set up

To reproduce and extend the analysis locally, you need R, RStudio and Quarto installed.

- R Version 4.5.1, renv.lock
- RStudio 2025.09.0 Build 387
- Quarto 1.8.26


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

If you need to extend the code and want to add a new library use the following steps to add libraries in a reproducable way:

```r
renv::install("<package>")
```

After installing the package and checking that your code works, you should call 

```r
renv::snapshot()
``` 
to record the latest package versions in your `renv.lock` lockfile. 

## License & Citation

This work is submitted as a Master Thesis at ZHAW. © 2026 Sarah Pfeiffer and licensed under [MIT License](LICENSE)





