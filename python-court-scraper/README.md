Coding Open-Source Generic Court Scraper
================

#### Object-oriented programming, bypassing Google Recaptcha

This code was written as part of a collaboration between the [Howard
Center for Investigative Journalism at the University of
Maryland](https://merrill.umd.edu/about-merrill/signature-programs/the-howard-center-for-investigative-journalism/)
and [Big Local News](https://biglocalnews.org/#/login) to write a
generic court-scraper that supports the most common court website
platforms.

[Last\_date.py](https://github.com/ryanelittle/work_samples/blob/main/python-court-scraper/last_date.py)
and
[search\_page\_mixin.py](https://github.com/ryanelittle/work_samples/blob/main/python-court-scraper/search_page_mixin.py)
are two base libraries that provide case discovery to the automated
scraping capabilities we are building. The latter instantiates the first
to provide the most recent case filed for a given year, county and case
type. It will skip weekends and holidays and, in the case of rarer
filings, look through multiple days until it finds the last case filed.
The mixin is designed to be inherited into a platform-specific search
page. It can be used with
[Selenium](https://selenium-python.readthedocs.io/) and
[Requests](https://requests.readthedocs.io/en/master/).

[Recaptcha\_v2.py](https://github.com/ryanelittle/work_samples/blob/main/python-court-scraper/recaptcha_v2.py)
is part of a captcha-handling library that uses a captcha-solving
service to bypass captchas on public court websites. This library
injects the response from the service into the page’s code and then
executes the submission using a given xpath or Javascript function. It
also accommodates an inheritance strategy that will allow a developer to
define their own submission script.
