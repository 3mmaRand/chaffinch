# chaffinch

This project is a demo for writing a report in Quarto. Below is an overview of the repository and pointers for getting started.

[HTML report](https://3mmarand.github.io/chaffinch/example-html.html)  
[PDF report](https://3mmarand.github.io/chaffinch/example-pdf.pdf)

## Overview
The chaffinch repository is a minimal Quarto project that demonstrates how to generate HTML and PDF reports from R code. At the top level you'll find sample Quarto documents (`example-html.qmd`, `example-pdf.qmd`), the raw dataset (`data-raw/chaff.txt`), reference materials (`references.bib`, `cell.csl`), images, a Quarto extension for PDF styling, and the rendered outputs.

## Project structure
- **Quarto documents**
  - `example-html.qmd` renders an HTML report using the tidyverse and broom packages.
  - `example-pdf.qmd` targets PDF output and demonstrates `titlepage-pdf` formatting.
- **Data**: `data-raw/chaff.txt` contains mass measurements for two chaffinch subspecies.
- **Extensions and assets**: `_extensions/nmfs-opensci/titlepage` provides LaTeX templates; `images/` holds photos; `QTDublinIrish.otf` supplies a custom font.

## Tips for getting started
1. **Render the examples:** run `quarto render example-html.qmd` or `quarto render example-pdf.qmd`.
2. **Explore YAML configuration:** review the YAML headers in the `.qmd` files to see cross-references, bibliographies, and formatting options.
3. **Work with the data:** the reports show a tidyverse workflow; try modifying the analyses or visualizations.
4. **Dig into the extension:** `_extensions/nmfs-opensci/titlepage` demonstrates how Quarto extensions bundle assets and templates.

## Next steps
- Learn more about Quarto’s layouts, cross-references, and publishing.
- Experiment with additional tidyverse tools or broom.
- Customize outputs by editing templates or adding CSS/LaTeX tweaks.

### PDF formatting example
You can customize page geometry and fonts by adding the following to the YAML header of a `.qmd` file:

```yaml
format:
  pdf:
    documentclass: article
    papersize: A4
    mainfont: Calibri
    geometry:
      - top=20mm
      - left=25mm
      - right=25mm
```
