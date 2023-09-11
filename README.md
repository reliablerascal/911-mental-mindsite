# 911 Mental Health Calls Coded as Violent
_A multi-city analysis of 911 mental health call coding_

This project looks at the proportion of mental-health-related 911 calls coded as violent vs. nonviolent.

The related story will be published at [MindSite News](https://mindsitenews.org/).

WHY this is important GILLOOLY Taylor, dispatched services. get into what I *don't* know

## Key Findings
Because call classification protocols and coding systems vary by city, numbers cannot be directly compared between cities. My key findings for each city based on their own classification systems are as follows:
* In **Cincinnati from 2017 to 2021**, 41% of calls classified as "mentally impaired" were coded as violent (MHRTV) as opposed to nonviolent (MHRT).
* In **Detroit from 2017 to 2021**, 70% of calls classified as "mental" were coded as either violent armed (MNTLARM) or violent not armed (MNTLNARM), as opposed to mental not violent (MENTPPRS).
* In **Boston in 2020**, 79% of calls classified as Emotionally Disturbed Person were coded as potentially violent (EDP2) as opposed to EDP3 (no indication of violence).

## Data sources
some mention re: Boston's police data
|Data Source|Description|
|---|---|
|[Cincinnati Open Data Portal- Police Calls for Service](https://data.cincinnati-oh.gov/safety/PDI-Police-Data-Initiative-Police-Calls-for-Servic/gexm-h6bt/data)|Desc|
|[Detroit Open Data Portal- Police Calls for Service](https://apis.detroitmi.gov/data/index.html) |Desc|
|[City of Boston Mental Health Emergency Calls Data Brief](https://www.boston.gov/sites/default/files/file/2021/08/Mental%20Health%20Call_Data%20Brief_FINAL_LB_edit.pdf)|Desc|

## Overview of Data Analysis Process
My data analysis process required the following steps:
* ...

% violent calls = (# violent mental health calls)/((# nonviolent mental health calls) + (# violent mental health calls))

## Limitations
Protocols, rulebooks, etc.
* ...

## What I Learned
...

I also learned:
* Socrata's API platform, commonly used in city data portals
* GitHub, a means of organizing and sharing my code
* Scaling back my emotionally-unregulated ambitions. I really wanted to delve into demographic patterns, but that will have to wait for a Part II.

## What I'd Like to Learn Next to Advance this Project
...

## Guide to the Repository
Most data for this project is collected directly in Python via API. You'll also find in this folder:
results includes exported data analysis

* [data](data/)- includes only my own manually-entered lookup table for CTA stations
* [Jupyter Notebook](notebooks/)- steps through the analysis
* [results](results/)- results output from Jupyter Notebook for mapping/charting in DataWrapper and Flourish