# 411-on-311
This document contains relevant information about our project including systematic code organization, visualization information / interpretations, & conclusions via statistical analysis and machine learning.

Files
ReadMe File (read_me.pdf), Master Doc (Python Pioneers DS GA 1007 Final Project.ipynb), Dataset Zip File (datasets.zip).
The Master Doc, which contains all of our code pertaining to the project, is a Jupyter Notebook titled Python Pioneers DS GA 1007 Final Project.ipynb. The original 311 Service Requests dataset (split into 15 datasets) which we merged into a master file that is read into the code, the StreetEasy Rent dataset, location categorization file, and zip code conversion file are zipped in datasets.zip. There are also four shape files used for the geopandas plots.

Merging & Cleaning Data
Python Pioneers DS GA 1007 Final Project.ipynb, cells 5 - 39.
In this component, we merge together the 311 Complaints dataset with the StreetEasy Rent dataset grouped by zip-code and created-date (month, year).
❖	Combine 15 separate Complaints datasets into one large dataset.
❖	Since the 15 separate files were large, we commented the code which merged them together. We begin by reading in the merged input file which was the output of the above merging code.
❖	Clean zip-codes (create a unique set of 5-digit zip-codes in NYC; remove zip-codes that are erroneous).
❖	Clean 311 Complaints dataframe.
❖	Merge neighborhood names, borough, population estimate, & median rent by date (month, year).
❖	Map neighborhood geometry zip-codes to cleaned zip-codes from merged dataframe.
❖	Prepare the merged dataframe for geoplots.

Visualizations
See Python Pioneers DS GA 1007 Final Project.ipynb, cells 40 - 96.
In this component, we create visualizations relating to complaints, rent, NYC area, pre/post covid analysis, and a combination of the aforementioned features in an effort to explore these relationships and patterns.
❖	Create a function that constructs horizontal bar graphs.
➢	Bar Graphs: top complaints in NYC across 2018-2022; priciest neighborhoods in NYC across 2018-2022; least complaint neighborhoods across 2018-2022.
❖	Create a function that constructs vertical bar plots.
➢	Bar Graphs: total number of complaints in NYC by year; average number of complaints in NYC by month.
❖	Generate side-by-side graphs displaying time-series analysis.
➢	Displays: top complaint types side-by-side for 2019, 2020, 2021; top complaint types vertically graphed for 2019, 2020, 2021.
❖	Generate line graphs showcasing shifts over time.
➢	Line Graphs: number of noise, heat, & rodent complaints across 2018-2022.
➢	Line Graphs: trend of total complaints compared to median rent across 2018-2022.
❖	Produce colored geoplots, mapping analysis to a neighborhood grid of NYC.
➢	Geo-Plots: number of rodent, heat, noise (with/without outlier), graffiti, food, new tree request, homeless person assistance, & streetlight condition complaints per ZCTA (zip-code tabulation area).
➢	Geo-Plots: average number of complaints by NYC borough.
❖	Conduct an in-depth pre/post COVID-19 time-series analysis.
➢	Geo-Plots: number of pre/post COVID complaints per ZCTA.
➢	Bar Graphs: top complaints (by total count) pre/post COVID.
❖	Define a function to build pie charts.
➢	Pie Charts: total number of noise, heat, & rodent complaints by borough.
➢	Pie Charts: total number of pre/post COVID complaints by borough.
❖	Design a function that creates scatter plots.
➢	Scatter Plots: median rent across 2018-2022 by borough.

Statistics
See Python Pioneers DS GA 1007 Final Project.ipynb, cells 97 - 108.
❖	Calculate rent averages, aggregates, & complaint counts by year.
❖	Calculate rent averages, aggregates, & complaint counts by NYC borough.
❖	Determine the average rent across recent years (2019-2022) to set classification threshold between “low” and “high” rent (or 0 and 1 in binary classification model).
❖	Compute Pearson Correlation between number of complaints and average rent.

Machine Learning
See Python Pioneers DS GA 1007 Final Project.ipynb, cells 109 - 121.
❖	Create a feature set consisting of total & yearly number of complaints by zip-code and binary labels (0 = low rent, 1 = high rent).
❖	Build a Logistic Regression model to classify a zip-code as containing either low rent (0) or high rent (1) properties on average.
❖	Build a Logistic Regression model to classify a zip-code as belonging to a certain NYC borough.
❖	Use validation metrics to determine efficacy of the model.

Findings & Conclusions
See Presentation slides.
❖	There are significant negative correlations between # of complaints & average rent.
❖	There are differing relationships between boroughs and top complaints.
❖	Rent and complaints differed before and after the COVID-19 pandemic.
❖	We can accurately classify rent and borough using data relating to complaints.


