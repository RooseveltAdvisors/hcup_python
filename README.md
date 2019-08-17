# HCUP + Python


This is a tutorial on working with Healthcare Cost and Utilization Project (HCUP) datasets using Python and other open-source alternatives to SAS and SPSS, which are the two primary data tools supported by HCUP.


The United States Agency for Healthcare Research and Quality has a variety of large, de-identified hospital patient datasets available via its Healthcare Cost and Utilization Project (aka HCUP). They contain broad information on the diagnoses, duration, and type of treatment per patient for each visit, and slightly more detailed information on the type and volume of charges. Because of this, and because HCUP also makes available a unique identifier that can be used to “follow” a patient within a given state, many physicians, epidemiologists, economists, and other researchers use them as a source for retrospective analysis of outcomes and cost-effectiveness.

That said, the data sets can be large enough to cause some headaches. A single year’s worth of the “core” emergency department visit data for the state of California is about 10 million rows in 152 columns, and arrives from HCUP in a 5.8GB flat (non-delimited) file. What’s more, the number and width of columns supplied varies by the state supplying the data, and even varies by year within a given state.

To aid in parsing the datasets, HCUP provides loading program definitions in SAS and SPSS formats. Unfortunately, not everyone has SAS or SPSS available, and even some who do may have needs best met by other environments or prefer to use open source alternatives. Whatever your particular reasons, if you are interested in working with HCUP data without SAS or SPSS, you’ll need some other way to parse, manipulate, and integrate them.

In my case, I am using the Python programing language (especially the excellent pandas library) to parse HCUP data sets and do preliminary cleanup, then a PostgreSQL database for integration and long-term storage. Much of the Python code I am using is rolled into a package called PyHCUP, which is available on PyPI or simply through pip (pip install PyHCUP).


## References:
- http://bielism.blogspot.com/2013/12/hcup-and-python-pt-i-background.html
- http://bielism.blogspot.com/2013/12/hcup-and-python-pt-4-reading-in-data.html
- http://bielism.blogspot.com/2013/12/hcup-and-python-pt-5-nulls-and-pre.html
- https://pypi.org/project/PyHCUP/
