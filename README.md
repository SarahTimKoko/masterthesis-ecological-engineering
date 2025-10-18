\# Masterthesis Ecological Engineering



\## Description





\## Project Structure

\- `R/` - R scripts

\- `data/raw` - raw data

\- `data/tidy` - clean data

\- `output/` - figures, tables, results

\- `\_site/` - generated html site

\- `\_site.yml` - R Markdown site configuration

\- `renv.lock` - environment lock file



\## Set up



```r

install.packages("renv")

```



\## Usage

```r

\# Load environment

renv::restore()



\# Run scripts

source("R/utils.R")



\# Render page

Rscript -e 'rmarkdown::render\_site()'

```

