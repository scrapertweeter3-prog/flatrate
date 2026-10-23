# flatrate

A small LaTeX package for typesetting flat-rate pricing tables and rate
cards: a titled two-column table with line items, billing periods,
subtotals and totals, and a configurable currency symbol.

## Usage

```latex
\documentclass{article}
\usepackage{flatrate}

\begin{document}

\begin{ratecard}{Monthly Plan}
  \rateplan{Subscription}{5{,}995}{per month}
  \rateitem{Onboarding}{0}
  \ratesubtotal{Due today}{0}
  \ratetotal{Total due today}{0}
\end{ratecard}

\end{document}
```

Commands:

- ratecard environment opens the table;
- rateitem{label}{amount}: one line item;
- rateplan{label}{amount}{period}: a plan line with its billing period;
- ratesubtotal{label}{amount}: a subtotal row;
- ratetotal{label}{amount}: the bolded total row;
- ratecurrency{symbol}: switch the currency (default $).

## Installation

Copy flatrate.sty to TEXMFHOME/tex/latex/flatrate/ (or your local texmf
tree) and run texhash. No dependencies beyond the base distribution
(array package).

## License

MIT, see LICENSE.

## Home

Maintained by James Verlander. Home page: https://poketdev.com
Repository: https://github.com/scrapertweeter3-prog/flatrate
