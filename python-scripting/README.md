Coding to Solve Journalistic Problems — Quickly
================

#### Using existing libraries to quickly code scripts, problem solve on deadline

These scripts were written as I first began implementing a more
functional style into the procedural scripts I was writing to acquire
the court data the Howard Center for Investigative Journalism used for
its [summer story on
evictions](https://www.usatoday.com/story/news/investigations/2020/09/02/cares-act-eviction-ban-confusion/5686217002/).

[Oklahoma-court-scraper.ipynb](https://github.com/ryanelittle/work_samples/blob/main/python-scripting/oklahoma-court-scraper.ipynb)
scrapes the [Oklahoma State Courts
Network](https://www.oscn.net/dockets/). In this form, it can be used to
scrape all evictions cases in Tulsa and Oklahoma counties using the
function oklahoma.scrapes\_cases().

[Address-parser.ipynb](https://github.com/ryanelittle/work_samples/blob/main/python-scripting/address-parser.ipynb)
was written to clean the defendant addresses scraped from six different
counties. The step was instrumental to increasing the percentage of
addresses that were successfully geocoded. This process allowed us to
assign evictions to neighborhoods and join the counts with U.S. Census
demographic information.
