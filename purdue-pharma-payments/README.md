Exposing Recipients of Purdue Pharma's Funding
================

#### Data analysis in R, novel logic pivoting, regex cleaning

Analysis of
[Purdue Pharma third-party funding](https://github.com/ryanelittle/work_samples/blob/main/purdue-pharma-payments/purdue-pharma-cleaning-and-analysis.Rmd)
was the first public accounting of the [$115 million Oxycontin marketing blitz](https://www.motherjones.com/crime-justice/2021/10/how-purdue-pharma-paid-out-to-politicians-and-pill-pushers/) — money that went to lobbying juggernauts, pain patient advocacy groups and even drug investigators and law enforcement groups.

The original 44-page [PDF](https://github.com/ryanelittle/work_samples/blob/main/purdue-pharma-payments/data/original-file-exhibit-88.pdf) was converted into 44 CSVs using Tabula. Errors were repaired using regex. Names were cleaned and broad names were created using OpenRefine. The CSV was pivoted into a database of payments using a custom parser written in Python that used the text's case to determine if a line was a company or a department.  Classifications were made in multiple passes with multiple reporters and editors contributing.
