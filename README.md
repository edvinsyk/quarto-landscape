# Landscape Extension For Quarto

The 'quarto-landscape' filter enables a landscape div, that switches the pages within the selection to landscape.
It implements the same div for docx, latex, and Typst, making it easier to switch between formats.

## Installing

```bash
quarto add edvinsyk/landscape
```

This will install the extension under the `_extensions` subdirectory.
If you're using version control, you will want to check in this directory.

## Using

Simply enclose what you want to have in landscape format using the landscape div.

Portrait format

::: {.landscape}
Landscape format
:::

Portrait format

This is commonly needed for displaying graphs or tables with dimensions when writing papers or content.
PDFs require the following in the YAML.

```{yaml}
format:
  pdf:
   include-in-header:
      text: |
        \usepackage{pdflscape}

```

## Example

Here is the source code for a minimal example: [example.qmd](example.qmd).

## Acknowledgements

Thanks to tarleb for the [word implementation](https://stackoverflow.com/questions/73784720/changing-page-orientation-in-word-using-quarto)