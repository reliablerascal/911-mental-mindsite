# 911 Mental Health Calls Coded as Violent
_A multi-city analysis of 911 mental health call coding_

This analysis looks at the proportion of mental-health-related 911 calls coded by call-takers as violent vs. nonviolent.

Such call classifications impact how cities handle mental health calls, reflect an assessment of potential risk to first responders, and impact whether someone suffering from a mental health crisis receives the help they need. In Boston, for example, a call classification of EDP3 (emotionally disturbed person, no indication of violence) can be handled by Emergency Medical Services alone, whereas a classification of EDP2 (emotionally disturbed person, potentially violent) requires police to first secure the scene before EMS arrives.

The importance of such call-coding has been underscored by research. Former police officer **Paul Taylor**, now an assistant professor at the University of Colorado, showed that police officers’ reactions to incidents in progress are [influenced by information relayed by 911 call-takers](https://journals-sagepub-com.turing.library.northwestern.edu/doi/10.1177/1098611119896653). This is true regardless of whether that information is accurate, though they’re unaware of this influence.

Research by former 911 call-taker **Jessica Gillooly**, now a 911 subject matter expert for the Department of Justice, called out [lack of clarity in dispatch rulebooks specifically related to mental health calls](https://onlinelibrary.wiley.com/doi/abs/10.1002/pam.22369), which affects the appropriateness of police response to mental health calls.



This analysis supports a story published in September 2023 at [MindSite News](https://mindsitenews.org/2023/09/11/911-call-takers-are-demoralized-overwhelmed-and-dealing-with-their-own-mental-health-woes/), [The Current](https://thecurrentga.org/2023/09/20/911-call-takers-are-demoralized-overwhelmed-and-dealing-with-their-own-mental-health-woes/), and [The Concord Monitor](https://articles.concordmonitor.com/911-Call-Takers-Are-Demoralized-Overwhelmed-and-Dealing-With-Their-Own-Mental-Health-Woes-52341576).


## Key Findings
Note that because call classification protocols and coding systems vary by city, proportions of calls flagged as violent cannot be directly compared between cities. My key findings for each city based on their own classification systems are as follows:
* In **Cincinnati from 2017 to 2021**, 41% of calls classified as "mentally impaired" were coded as violent (MHRTV) as opposed to nonviolent (MHRT).
* In **Detroit from 2017 to 2021**, 70% of calls classified as "mental" were coded as either "violent armed" (MNTLARM) or "violent not armed" (MNTLNARM), as opposed to "mental not violent" (MENTPPRS).
* In **Boston in 2020**, 79% of calls classified as "emotionally disturbed person" (EDP) were coded as "potentially violent" (EDP2) as opposed to no indication of violence (EDP3).

## Data sources
|Data Source|Description|
|---|---|
|[Cincinnati Open Data Portal- Police Calls for Service](https://data.cincinnati-oh.gov/safety/PDI-Police-Data-Initiative-Police-Calls-for-Servic/gexm-h6bt/data)|All Cincinnati Police Department Calls for Service|
|[Detroit Open Data Portal- Police Calls for Service](https://apis.detroitmi.gov/data/index.html) |Downloadable archive of Detroit Police Department Calls for Service|
|[Boston Mental Health Emergency Calls Data Brief](https://www.boston.gov/sites/default/files/file/2021/08/Mental%20Health%20Call_Data%20Brief_FINAL_LB_edit.pdf)|Data brief summarizing mental health emergency calls, classified as EDP2 or EDP3|
|[Boston Emergency Medical Services 2020 Vital Statistics](https://www.boston.gov/sites/default/files/file/2022/04/2020-Vital-Stats-Boston-EMS.pdf)|2020 Vital Statistics for Boston, showing exact count of "psychological/suicidal" calls|

## Overview of Data Analysis Process
My data analysis process required the following steps:
* Identifying call categories specific to mental health
* Extracting related 911 call data for each city
* Calculating the proportion of 911 mental health calls flagged as violent or potentially violent:

<table><tr><td rowspan="2">% violent calls = </td><td>(# violent mental health calls)</td></tr>
<tr><td>(# nonviolent mental health calls) + (# violent mental health calls)</td></tr></table>

## Limitations and Next Steps to Advance this Project
A key limitation of this analysis is that identification of mental health calls may be missed entirely in the data. This is particularly true where call-takers haven't been trained to identify mental-health-related calls, as suggested by an [analysis by the Vera Institute](https://www.vera.org/downloads/publications/911-analysis-civilian-crisis-responders.pdf) and underscored by the National Emergency Number Association's own finding that nearly a quarter of survey respondents feel [unprepared to deal with mental health calls](https://the-pulse-of-9-1-1-2023.carbyne.com/?utm_source=Press+Release&utm_medium=Press+Release&utm_campaign=GUI_Survey_Results_Pulse_of_911_PS_US_Q323&utm_id=GUI_Survey_Results_Pulse_of_911_PS_US_Q323_PR&utm_term=Pulse).

A closer look at call-taker protocols and training is required for deeper insight into how 911 operators in each city identify mental health calls, and determine whether the situation is violent or nonviolent. Interviews with call-takers could also provide additional insight.

## Guide to the Repository
This repository includes the following:

* [data](data/)- 911 call data acquired from cities, as well as downloads and screenshots of Boston's mental health emergency calls report.
* [Jupyter Notebook](911_mental_violent_rates.ipynb)- reproducible steps for analyzing 911 call data in Python
