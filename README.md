Work Samples
================

This repository exists to show examples of the code I have written as a
data reporter at [Mother Jones](https://www.motherjones.com), the [Howard Center for Investigative Journalism at the University of Maryland](https://merrill.umd.edu/about-merrill/signature-programs/the-howard-center-for-investigative-journalism/), ProPublica and the Associated Press' election web scraping team.

I am a journalist who specializes in using computational and analytical tools in the application of the scientific method to answer journalistic questions. I love working with others to solve problems and especially enjoy learning new and better ways to execute this process. My results are compelling, character-driven stories that personify data findings into memorable narratives that matter, like a homeless man from a Florida beach town whose story ultimately ended up on [John Oliver’s Last Week Tonight](https://www.youtube.com/watch?v=liptMbjF3EE).

I write agile, object-oriented Python, functional R using the Tidyverse and have built and analyzed SQL databases with millions of rows. I have experience working with many types of data, including massive government datasets, court records and small spreadsheets built by the reporting of a team of journalists. My analyses have included the use of linear regressions and other statistical models, demonstrating correlation and other newsworthy relationships.

All of the code in this repository was written by me.

- [Data Analysis in R](#data)
- [Coding on Deadline](#python)
- [Coding Open-Source Generic Court Scraper](#object)
- [About Me](#about)
- [Resume](https://media.journoportfolio.com/users/52314/uploads/f6e5aceb-1874-4e87-bac3-1b3536551b8b.pdf)
- [Website](https://www.ryanerinlittle.com)

<a id="data"></a>

## Analysis of Court Records

#### Data cleaning, analysis in R, writing, traditional reporting

Analysis of
[okaloosa-criminal-records-analysis.rmd](https://github.com/ryanelittle/work_samples/blob/main/court-records-analysis/okaloosa-criminal-records-analysis.Rmd) led to the core findings of the Howard Center for Investigative
Journalism’s story on the [criminalization of homelessness](https://apnews.com/article/571a8646896ed0d12f3fe7ca3b1d064d), which found trespassing charges had become the key law cities across the country were using to forbid homeless people from public and quasi-public places. The data also revealed our lead character.

Before I found Kenneth Ivan Shultz III on the streets of Fort Walton Beach, Fla., I found the
homeless man at the top of this data analysis. The 71-year-old retiree has spent one of every three nights in jail since he became homeless nine years ago. He was charged with trespassing 96 times. As of June 29, 2020, he had spent 1,034 days in jail. He owed $41,311 in court costs. His story was retold on [John Oliver’s Last Week Tonight](https://www.youtube.com/watch?v=liptMbjF3EE).

This analysis also created a searchable database that informed my on-the-ground reporting on a March 2020 reporting trip I was ordered home early from because of the pandemic. The database allowed me to search criminal histories as I met individual homeless people on the ground.

## Analysis of Voting Database

#### Data cleaning, analysis in R

My [analysis of Georgia voting data](https://github.com/ryanelittle/work_samples/blob/main/voting-records-analysis/georgia-analysis.Rmd) showed shows that the number of voters disenfranchised by rejected mail ballot applications skyrocketed after the GOP-controlled legislature passed sweeping new restrictions on mail voting last year. During municipal elections in November, Georgia voters were 45 times more likely to have their mail ballot applications rejected—and ultimately not vote as a result—than in 2020.

The work was a deeper look at an analysis by the Atlanta Journal-Constitution in November 2021 that found rejected mail ballot applications had quadrupled compared to 2020. Where AJC asked what the rejection rate was, Mother Jones asked how many voters wanted a ballot but did not get one because their request(s) were ultimately rejected by election officials. I was able to see if voters ultimately voted by mail or in-person by joining voter history to the absentee voter data.

## Exposing Recipients of Purdue Pharma's Funding

#### Data analysis in R, novel logic pivoting, regex cleaning

Analysis of [Purdue Pharma third-party funding](https://github.com/ryanelittle/work_samples/blob/main/purdue-pharma-payments/purdue-pharma-cleaning-and-analysis.Rmd) was the first public accounting of the [$115 million Oxycontin marketing blitz](https://www.motherjones.com/crime-justice/2021/10/how-purdue-pharma-paid-out-to-politicians-and-pill-pushers/) — money that went to lobbying juggernauts, pain patient advocacy groups and even drug investigators and law enforcement groups.

The original 44-page [PDF](https://github.com/ryanelittle/work_samples/blob/main/purdue-pharma-payments/data/original-file-exhibit-88.pdf) was converted into 44 CSVs using Tabula. Errors were repaired using regex. Names were cleaned and broad names were created using OpenRefine. The CSV was pivoted into a database of payments using a custom parser written in Python that used the text's case to determine if a line was an organization or a department. Classifications were made in multiple passes with multiple reporters and editors contributing.

<a id="python"></a>

## Coding on Deadline

#### Using existing libraries to quickly code scripts, problem-solve on deadline

[apache-rehost-script.ipynb](https://github.com/ryanelittle/work_samples/blob/main/coding-on-deadline/apache-rehost-script.ipynb) was written to solve a problem I had trying to scrape election results during the 2020 U.S. presidential election. The Associated Press has a scraping rig it uses to automate the collection of election results for counties across the country. It handles many file types, including PDFs, HTML and XML. But it can't scrape PDFs that are hosted on an FTP server or Google Drive. This script worked around that limitation by downloading the PDF on my computer and pushing it to my GitHub every 60 seconds. We pointed the AP program at my GitHub instead of the election site. The solution guaranteed AP and its readers would get updates on crucial votes as quickly as possible.

[Address-parser.ipynb](https://github.com/ryanelittle/work_samples/blob/main/coding-on-deadline/address-parser.ipynb) was written to clean the defendant addresses scraped from six different counties. The step was instrumental to increasing the percentage of addresses that were successfully geocoded. This process allowed us to assign evictions to neighborhoods and join the counts with U.S. Census demographic information.

<a id="object"></a>

## Coding Open-Source Court Scraper

#### Object-oriented programming, bypassing Google Recaptcha

This code was written as part of a collaboration between the [Howard Center for Investigative Journalism at the University of Maryland](https://merrill.umd.edu/about-merrill/signature-programs/the-howard-center-for-investigative-journalism/) and [Big Local News](https://biglocalnews.org/#/login) to write a generic [court-scraper](https://github.com/biglocalnews/court-scraper) that supports the most common court website platforms.

[Last\_date.py](https://github.com/ryanelittle/work_samples/blob/main/python-court-scraper/last_date.py)
and [search\_page\_mixin.py](https://github.com/ryanelittle/work_samples/blob/main/python-court-scraper/search_page_mixin.py) are two base libraries that provided case discovery to the automated scraping capabilities. The latter instantiates the first to provide the most recent case filed for a given year, county and case type. It will skip weekends and holidays and, in the case of rarer filings, look through multiple days until it finds the last case filed. The mix-in is designed to be inherited into a platform-specific search page. It can be used with [Selenium](https://selenium-python.readthedocs.io/) and [Requests](https://requests.readthedocs.io/en/master/).

[Recaptcha\_v2.py](https://github.com/ryanelittle/work_samples/blob/main/python-court-scraper/recaptcha_v2.py) is part of a captcha-handling library that uses a captcha-solving service to bypass captchas on public court websites. This library injects the response from the service into the page’s code and then executes the submission using a given xpath or Javascript function. It also accommodates an inheritance strategy that will allow a developer to define their own submission script.


<a id="about"></a>

## About me

I am an award-winning data journalist and the Roy W. Howard Fellow at [Mother Jones](https://www.motherjones.com). I also do contract work with ProPublica and the Associated Press' election web scraping team.

I previously worked at the [Howard Center for Investigative Journalism](https://merrill.umd.edu/howard-center-for-investigative-journalism), the [Capital News Service](https://cnsmaryland.org/) and [The Ledger](https://www.theledger.com/) in Lakeland, Fla. My work has appeared in the New York Times, Washington Post, Associated Press and elsewhere.

I have a master’s degree from the [Philip Merrill College of Journalism at the University of Maryland](https://merrill.umd.edu/). There, I focused my studies on computational and data journalism. My undergraduate degree is from the [Nicholson School of Communication and Media at the University of Central Florida](https://communication.ucf.edu/), where I studied journalism and public administration.
