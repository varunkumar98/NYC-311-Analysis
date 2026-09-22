NYC 311 Service Request Analysis
Interactive Tableau analysis of New York City's 311 non-emergency service request data, examining how complaint volume, agency response times, and reporting patterns shifted before and during the COVID-19 pandemic.

Tool Data%20Processing Scope

Overview
NYC's 311 system lets residents report non-emergency issues — noise complaints, graffiti, potholes, illegal dumping, tree-trimming requests, and more — by phone, website, or app. This project builds an interactive Tableau dashboard over the full public 311 dataset to explore complaint patterns across NYC's boroughs and agencies, with a focus on how the pandemic changed things.

The raw dataset spans 2010–2022 and contains 30+ million records (~18 GB). Because a dataset that size is impractical to clean with Pandas/Jupyter alone, the data was processed in Google BigQuery and reduced to a more workable ~2.5 GB (~12 million records) for the in-depth 2017–2022 analysis, then visualized in Tableau.

This was a group project for IE6600 – Computation and Visualization at Northeastern University.

Research Questions
The dashboards were built around six guiding questions:

Does the Pareto Principle apply to 311 complaints? — i.e., do a small number of complaint types account for the majority of calls.
Is population directly correlated with 311 complaint volume? — Surprisingly, no: the Bronx, the second-least-populated borough, recorded the highest number of noise complaints.
Do people become more tolerant during the holiday season? — Complaint volume rose during COVID in most months, but dipped in October–December; the data can't confirm this is due to seasonal tolerance rather than other factors.
Did COVID actually impact the efficiency of NYC agencies? — Yes: response times dropped noticeably during COVID, with agencies like the NYPD and DCA (Department of Consumer Affairs) responding faster than pre-pandemic.
Did COVID impact the volume of 311 requests? — Yes, request volume rose moderately during COVID compared to before.
Do New Yorkers sleep at night? — Noise complaints spike after 8 p.m., suggesting a lot of late-night reporting.
Repository Contents
File	Description
Group-3_Project__Report.pdf	Full written report: introduction, methodology, research questions, findings, and limitations/future scope.
311_viz_14-12-22.twb	Main Tableau workbook with the interactive dashboards.
Flow1-grouping complaint types.tfl, Flow2 - data prep 10-12-22.tfl, final flow 11-12-22.tfl	Tableau Prep flows used to clean and reshape the raw data.
CViz_Project_Proposal (1).pptx	Initial project proposal deck.
CViz_Project_Progress_2-1.pptx	Mid-project progress presentation.
CViz_Final_PPT_grp_3.pptx	Final presentation deck.
Tech Stack
Google BigQuery — cleaning and aggregating the 30M+ row source dataset
Tableau Desktop / Tableau Prep — dashboarding and data-flow transformations
Python (Pandas) — supplementary data pre-processing
Getting Started
To explore the dashboards yourself:

Install Tableau Desktop (or use Tableau Public if the workbook doesn't rely on a live data connection).
Open 311_viz_14-12-22.twb.
Use the in-dashboard filters (borough, complaint type, zip code, year) to explore responsiveness and complaint trends for 2017–2022.
The .tfl files can be opened in Tableau Prep to see how the raw NYC Open Data 311 export was cleaned and joined.

Limitations & Future Scope
The in-depth analysis covers 2017–2022; extending the full 2010–2022 range is limited by the size of the raw data (~18 GB / 30M+ rows).
A natural next step is a machine-learning model to forecast complaint volume, to help agencies plan resource allocation.
More compute would allow richer, higher-resolution analysis across additional variables.
Team
Group project for IE6600 (Group 3): Saravanan Arumugam, Satyajit Lanka, Shriram Vijaykumar, and Varun Kumar Kumaravel.
