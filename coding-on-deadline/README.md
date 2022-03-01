Coding on Deadline
================

#### Using existing libraries to quickly code scripts, problem-solve on deadline

[apache-rehost-script.ipynb](https://github.com/ryanelittle/work_samples/blob/main/python-scripting/apache-rehost-script.ipynb) was written to solve a problem I had trying to scrape election results during the 2020 U.S. presidential election. The Associated Press has a scraping rig it uses to automate the collection of election results for counties across the country. It handles many file types, including PDFs, HTML and XML. But it can't scrape PDFs that are hosted on an FTP server or Google Drive. This script worked around that limitation by downloading the PDF on my computer and pushing it to my GitHub every 60 seconds. We pointed the AP program at my GitHub instead of the election site. The solution guaranteed AP and its readers would get updates on crucial votes as quickly as possible.

[Address-parser.ipynb](https://github.com/ryanelittle/work_samples/blob/main/python-scripting/address-parser.ipynb) was written to clean the defendant addresses scraped from six different counties. The step was instrumental to increasing the percentage of addresses that were successfully geocoded. This process allowed us to assign evictions to neighborhoods and join the counts with U.S. Census demographic information.

## Exposing Recipients of Purdue Pharma's Funding
#### Data analysis in R, novel logic pivoting, regex cleaning

Analysis of [Purdue Pharma third-party funding](https://github.com/ryanelittle/work_samples/blob/main/purdue-pharma-payments/purdue-pharma-cleaning-and-analysis.Rmd) was the first public accounting of the [$115 million Oxycontin marketing blitz](https://www.motherjones.com/crime-justice/2021/10/how-purdue-pharma-paid-out-to-politicians-and-pill-pushers/) — money that went to lobbying juggernauts, pain patient advocacy groups and even drug investigators and law enforcement groups.

The original 44-page [PDF](https://github.com/ryanelittle/work_samples/blob/main/purdue-pharma-payments/data/original-file-exhibit-88.pdf) was converted into 44 CSVs using Tabula. Errors were repaired using regex. Names were cleaned and broad names were created using OpenRefine. The CSV was pivoted into a database of payments using a custom parser written in Python that used the text's case to determine if a line was an organization or a department. Classifications were made in multiple passes with multiple reporters and editors contributing.
