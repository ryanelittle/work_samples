Work Samples
================
Ryan E. Little
10/5/2020

## Overview

This repository exists to show examples of the code I have written as a
data reporter at the [Howard Center for Investigative Journalism at the
University of
Maryland](https://merrill.umd.edu/about-merrill/signature-programs/the-howard-center-for-investigative-journalism/).

These code samples have been chosen to show my growth as a computational
journalist since first learning the basics of the Tidyverse in August
2019.

Before I began my graduate education at the [Philip Merrill College of
Journalism](https://merrill.umd.edu/), I knew almost nothing about
coding. As of October 2020, I am coding an open-source court scraper
that my collaborators and I hope will make the web-scraping of U.S.
court websites more accessible to local news reporters.

All of the code in this repository was written by me.

## Object-Oriented Programming<a id="object"></a>

This code was written as part of a collaboration between the Howard
Center for Investigative Journalism and
[BigLocalNews](https://biglocalnews.org/#/login) to write a generic
court-scraper that supports the most common court website platforms.

[Last\_date.py](https://github.com/ryanelittle/work_samples/blob/main/python-oop-coding/last_date.py)
and
[search\_page\_mixin.py](https://github.com/ryanelittle/work_samples/blob/main/python-oop-coding/search_page_mixin.py)
are two base libraries that provide case discovery to the automated
scraping capabilities we are building. The latter instantiates the first
to provide the most recent case filed for a given year, county and case
type. It will skip weekends and holidays and, in the case of rarer
filings, look through multiple days until it finds the last case filed.
The mixin is designed to be inherited into a platform-specific search
page. It can be used with
[Selenium](https://selenium-python.readthedocs.io/) and
[Requests](https://requests.readthedocs.io/en/master/).

[Recaptcha\_v2.py](https://github.com/ryanelittle/work_samples/blob/main/python-oop-coding/recaptcha_v2.py)
is part of a captcha-handling library that uses a captcha-solving
service to bypass captchas on public court websites. This library
injects the response from the service into the page’s code and then
executes the submission using a given xpath or Javascript function. It
also accommodates an inheritance strategy that will allow a developer to
define their own submission script.

## Python Scripts<a id="python"></a>

These scripts were written as I first began implementing a more
functional style into the procedural scripts I was writing to acquire
the court data the Howard Center for Investigative Journalism used for
its [summer story on
evictions](https://www.usatoday.com/story/news/investigations/2020/09/02/cares-act-eviction-ban-confusion/5686217002/).

[Oklahoma-court-scraper.ipynb](https://github.com/ryanelittle/work_samples/blob/main/python-early-scripting/oklahoma-court-scraper.ipynb)
scrapes the [Oklahoma State Courts
Network](https://www.oscn.net/dockets/). In this form, it can be used to
scrape all evictions cases in Tulsa and Oklahoma counties using the
function oklahoma.scrapes\_cases().

[Address-parser.ipynb](https://github.com/ryanelittle/work_samples/blob/main/python-early-scripting/address-parser.ipynb)
was written to clean the defendant addresses scraped from six different
counties. The step was instrumental to increasing the percentage of
addresses that were successfully geocoded. This process allowed us to
assign evictions to neighborhoods and join the counts with U.S. Census
demographic information.

## Data Analysis in R<a id="data"></a>

Analysis of
[okaloosa-criminal-records-analysis.rmd](https://github.com/ryanelittle/work_samples/blob/main/data-analysis-in-r/okaloosa-criminal-records-analysis.Rmd)
led to the core findings of the Howard Center for Investigative
Journalism’s story on the [criminalization of
homelessness](https://apnews.com/article/571a8646896ed0d12f3fe7ca3b1d064d).
It turned out the same trends identified here were true in other parts
of the country.

The data also revealed our lead character. Before I found Kenneth Ivan
Shultz III on the streets of Fort Walton Beach, Fla., I found the
homeless man on the top of this data analysis. The 71-year-old retiree
has spent one of every three nights in jail since he became homeless
nine years ago.

He was charged with trespassing 96 times. As of June 29, 2020, he had
spent 1,034 days in jail. He owed $41,311 in court costs.

This analysis also created a searchable database that informed my
on-the-ground reporting on a March reporting trip I was ordered home
early from because of the pandemic. The database allowed me to search
criminal histories as I met individual homeless people on the ground.
