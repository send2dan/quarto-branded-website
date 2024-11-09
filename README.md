> [!IMPORTANT]
> 
> This is **not** an official Stanford University project. This is part of a demonstration for STATS 290 regarding Quarto portfolio websites and brands!

# Stanford Brand Demo - Quarto

This repository shows an implementation of [Stanford's identity guidelines][suidg] with [Quarto][qmain] using the new [`brand.yml` specification][byml] in [Quarto pre-release v1.6][qbyml] This provides a reusable way for creating consistent Stanford-branded academic and technical content across different output formats including HTML documents, RevealJS presentations, Typst documents, and dashboards.

> [!NOTE]
>
> This demo is using **pre-release** versions of Quarto and the `brand.yml` specification. The final release may have changes to the specification and implementation.
> If you wish to use this in your own projects, please make sure you have a [pre-release version of Quarto](https://quarto.org/docs/download/prerelease.html) and refer to the official documentation for the latest information.

## Overview

The demo showcases Stanford's identity guidelines through different Quarto documents:

- HTML
- RevealJS
- Typst
- Dashboard

> [!NOTE]
>
> This demo is based on the [Example Brand Demo](https://github.com/cwickham/quarto-examples/tree/brand/brand/brand-simple) by Charlotte Wickham discussed in the [Quarto Branding Documentation][qbyml].

### Requirements

- [Quarto][qmain] > 1.6.32

> [!IMPORTANT]
>
> Figure out why the brand theme isn't being applied to the top navigation bar.

## Structure

```
.
├── README.md          # This documentation
├── _brand.yml         # Stanford brand specifications
├── _quarto.yml        # Quarto project configuration
└── index.qmd          # Example document
```

## Brand Implementation

The [`_brand.yml` file][byml] defines Stanford's visual identity elements:

- Cardinal Red as primary color
- Cool Grey as secondary color
- Source Sans Pro and Source Serif Pro fonts
- Spacing and layout guidelines
- Custom color variants and tints

Example from `_brand.yml`:

```yaml
color:
  primary: "#8C1515"    # Stanford Cardinal Red
  secondary: "#4D4F53"  # Cool Grey
  success: "#175E54"    # Dark Green
  info: "#006CB8"       # Digital Blue
  warning: "#FFBD3D"    # Sun
  danger: "#820000"     # Dark Cardinal Red
```

We register the brand configuration in the project's `_quarto.yml` with:

```yaml
brand: _brand.yml
```



## Usage

1. Clone this repository:
   ```bash
   git clone git@github.com:stanford-brand-yml/quarto-branded-website.git
   ```

2. Create your content in `.qmd` files using the Stanford brand elements.

3. Preview your project:
   ```bash
   quarto preview
   ```

## Acknowledgments

- [Stanford University Identity Guide][suidg]
- Quarto Team for implementing the `brand.yml` specification


[suidg]: https://identity.stanford.edu/
[qmain]: https://quarto.org/
[byml]: https://posit-dev.github.io/brand-yml/
[qbyml]: https://prerelease.quarto.org/docs/authoring/brand.html

