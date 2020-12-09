# Matplotlib Homework - The Power of Plots

## Background

![Laboratory](Images/Laboratory.jpg)

Base on data from Pymaceuticals Inc., a burgeoning pharmaceutical company based out of San Diego. Pymaceuticals specializes in anti-cancer pharmaceuticals. In its most recent efforts, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.

A extended data analisis from the access to the complete data from their most recent animal studyhas been requested. In this study, 249 mice identified with SCC tumor growth were treated through a variety of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals' drug of interest, Capomulin, versus the other treatment regimens. It have been tasked by the executive team to generate all of the tables and figures needed for the technical report of the study. The executive team also has asked for a top-level summary of the study results.

## Solutions

Full detail of the solution can be found in the Pymaceuticals script  [Pymaceuticals script](Pymaceuticals/pymaceuticals.ipynb)

### Data Cleaning

* Before beginning the analysis, the data was checked for any mouse ID with duplicate time points and  any data associated with that mouse ID was removed. Cleaned data was used for the remaining steps. The head (5 rows on the top) of cleaned data is shown below.

[clean data](Images/data_combined_clean_head.png)

### Summary statistics

* A summary statistics table consisting of the mean, median, variance, standard deviation, and SEM of the tumor volume for each drug regimen was generated. 

[summary statistics](Images/summary_statistics.png)

### Bar Charts and Pie Charts

*  Two identical bar plot using two methods (Pandas's `DataFrame.plot()` and Matplotlib's `pyplot`) that shows the total number of measurements taken for each treatment regimen throughout the course of the study were generated.

Pandas's `DataFrame.plot()`

[pandas bar plot](Images/bar_plot_pandas.png)

Matplotlib's `pyplot

[pyplot bar plot](Images/bar_plot_pyplot.png)


*  Two identical pie plot using two methods (Pandas's `DataFrame.plot()` and Matplotlib's `pyplot`) that shows the distribution of female or male mice in the study were generated.

Pandas's `DataFrame.plot()`

[pandas pie plot](Images/pie_plot_pandas.png)

Matplotlib's `pyplot

[pyplot pie plot](Images/pie_plot_pyplot.png)

### Quartiles, Outliers and Boxplots

* Final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Calculate the quartiles and IQR and quantitatively determination of any potential outliers across all four treatment regimens. 

Final Tumor Volume for all four treatment regimens. The head (5 rows on the top) of summary table is shown below.

[final tumor vol best regimens](Images/final_tumor_vol_best_regimens_head.png)

Quartiles and IQR and quantitatively determination of any potential outliers across all four treatment regimens.

IQR for Capomulin: 7.78
Lower Bound for Capomulin: 20.71
Upper Bound for Capomulin: 51.83
Number of Capomulin outliers: 0
IQR for Ramicane: 9.1
Lower Bound for Ramicane: 17.91
Upper Bound for Ramicane: 54.31
Number of Ramicane outliers: 0
IQR for Infubinol: 11.48
Lower Bound for Infubinol: 36.83
Upper Bound for Infubinol: 82.75
Number of Infubinol outliers: 1
IQR for Ceftamin: 15.58
Lower Bound for Ceftamin: 25.35
Upper Bound for Ceftamin: 87.67
Number of Ceftamin outliers: 0

* A box and whisker plot of the final tumor volume for all four treatment regimens was generated, and a potential outliers highlighted by using color, and style.

[box plot](Images/box_plot_best_regimens.png)


### Line ad Scatter Plots

* A line plot of tumor volume vs. time point for a random mouse that was treated with Capomulin was generated.

[line plot](Images/line_plot_Capomulin.png)


* A scatter plot of mouse weight versus average tumor volume for the Capomulin treatment regimen was generated.

[line plot](Images/scatter_plot_capomulin.png)

### Correlation and Regression

* The correlation coefficient and linear regression model between mouse weight and average tumor volume for the Capomulin treatment was calculated. The linear regression model on top of the previous scatter plot was generated.

[regression](Images/regression_plot_capomulin.png)


## Observations and Insights

*  The hight number of data points for each Drug Regimen shows a good sample distribution which allows to obtain good statistical results.

* The gender pie plot shows that study had a near identical number of male and female mice. Determining if sex of the mouse was correlated to efficacy would be interesting to look at.

* The box and whisker plot shows that the effectiveness of Capomulin seems to be comparable to Ramicane, and it is significantly more effective than Infubinol and Ceftamine. Also, The results of the analysis are very consistent and there is only 1 outlier in the data set for Infubinol.

* The regression analysis shows how much the average tumor volume will change when weight of mice change. The R-squared value is 0.70, which means 70% the model fit the data.

### Copyright

Trilogy Education Services © 2020. All Rights Reserved.