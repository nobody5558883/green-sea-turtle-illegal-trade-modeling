# Data Guide

## Required Files

Place these files in this directory:

| Filename | Required fields | Use |
|---|---|---|
| `cites_term_2014_2023.csv` | `Ranking`, `Term`, `Quantity`, `Filters` | Trade-term summary |
| `cites_source_2014_2023.csv` | `Ranking`, `Source`, `Code`, `2014` through `2023`, `Filters` | Annual wild-source time series |
| `cites_taxonomic_group_2014_2023.csv` | `Ranking`, `Taxonomic Group`, `Quantity`, `Kingdom`, `Phylum`, `Class`, `Order`, `Family`, `Genus`, `Taxon`, `Filters` | Taxonomic aggregation and PCA |

## Source and Scope

The supplied files are CITES Wildlife TradeView exports downloaded on February 2, 2024. Their filter metadata identifies exporter-reported, direct, wild-sourced mammal specimens measured as numbers of specimens for 2014–2023.

These are filtered aggregate exports, not individual trade transactions. The files do not establish that a record represents illegal trade, and the taxonomic export is not limited to green sea turtles.

## Data-Quality Notes

- The term export contains 51 rows and no missing values in the supplied copy.
- The source export contains one wild-source row and annual values for 2014–2023.
- The raw taxonomic export contains 501 rows. In the supplied copy, `Order`, `Family`, and `Genus` contain 1, 5, and 12 missing values, respectively. The notebook labels these values `Unknown` rather than inferring a biological classification.
- The 2023 annual quantity is zero. Because this could indicate an incomplete reporting period, the forecasting notebook excludes 2023 from model fitting and displays it separately.

## Reuse and Attribution

Confirm the current CITES Trade Database or TradeView terms before redistributing source exports publicly. If redistribution is not permitted or is unclear, remove the CSV files from GitHub and retain this guide so users can download equivalent exports from the official source.

