# Landscape Extension For Quarto

> [!IMPORTANT]  
> This extension has been merged into quarto version 1.6.6. (see. quarto-dev/quarto-cli#10581) and should work out of the box.

The 'quarto-landscape' filter enables a landscape div, that switches the pages within the selection to landscape.
It implements the same div for docx, latex, and Typst, making it easier to switch between formats.

## Installing

```bash
quarto add edvinsyk/quarto-landscape
```

This will install the extension under the `_extensions` subdirectory.
If you're using version control, you will want to check in this directory.

## Using

Simply enclose what you want to have in landscape format using the landscape div.

```{markdown}
Portrait format

::: {.landscape}

Landscape format

:::

Portrait format
```

This is commonly needed for displaying graphs or tables with dimensions when writing papers or content.
PDFs require the following in the YAML.

## Required in YAML

The following is required in YAML for the extension to work:

 ```{yaml}
# Required for all:
filters:
  - landscape

# Required for PDF:

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
