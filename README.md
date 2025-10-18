# Masterthesis Ecological Engineering

## Description

The results of this project is automatically deployed to <https://sarahtimkoko.github.io/masterthesis-ecological-engineering>

## Project Structure

-   `R/` - R scripts
-   `data/raw` - raw data
-   `data/tidy` - clean data
-   `output/` - figures, tables, results
-   `\_site/` - generated html site
-   `\_site.yml` - R Markdown site configuration
-   `renv.lock` - environment lock file

## Set up

``` r
install.packages("renv")
```

## Usage

``` r
# Load environment
renv::restore()

# Run scripts

source("R/utils.R")

```

## Install new package with renv

```r
renv::install("<package>")
```

After installing the package and checking that your code works, you should call 
```r
renv::snapshot()
``` 
to record the latest package versions in your lockfile. 

## Rendering the Site Locally

### Method 1: Using RStudio
1. Open the project in RStudio
2. Click "Build" -> "Render Website"
   Or use keyboard shortcut Ctrl+Shift+B (Windows/Linux) or Cmd+Shift+B (Mac)

### Method 2: Using Command Line
```bash
# Render the site
quarto preview

# Or for a full build
quarto render
```

Note: 
- `quarto preview` starts a local server with live preview
- `quarto render` builds the site without starting a server
- The rendered site will be in the `_site` directory

