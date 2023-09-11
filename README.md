# Matplotlib Challenge: Pymaceuticals

**Student name:** Tania Barrera

---

- [Background](#background)
- [Instructions and Requirements](#instructions-and-requirements)
  - [Prepare the Data *(20 points)*](#prepare-the-data-20-points)
  - [Generate Summary Statistics *(15 points)*](#generate-summary-statistics-15-points)
  - [Create Bar Charts and Pie Charts *(15 points)*](#create-bar-charts-and-pie-charts-15-points)
  - [Calculate Quartiles, Find Outliers, and Create a Box Plot *(30 points)*](#calculate-quartiles-find-outliers-and-create-a-box-plot-30-points)
  - [Create a Line Plot and a Scatter Plot *(10 points)*](#create-a-line-plot-and-a-scatter-plot-10-points)
  - [Calculate Correlation and Regression *(10 points)*](#calculate-correlation-and-regression-10-points)


---

This repo contains my work for the fifth weekly challenge of the UofT SCS edX Data Bootcamp.

---

**From bootcampspot:**

What good is data without a good plot to tell the story?

In this assignment, you’ll apply what you've learned about Matplotlib to a real-world situation and dataset.

## Background

You've just joined Pymaceuticals, Inc., a new pharmaceutical company that specializes in anti-cancer medications. Recently, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.

As a senior data analyst at the company, you've been given access to the complete data from their most recent animal study. In this study, 249 mice who were identified with SCC tumors received treatment with a range of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals’ drug of interest, Capomulin, against the other treatment regimens.

The executive team has tasked you with generating all of the tables and figures needed for the technical report of the clinical study. They have also asked you for a top-level summary of the study results.

## Instructions and Requirements

This assignment is broken down into the following tasks:

- Prepare the data.

- Generate summary statistics.

- Create bar charts and pie charts.

- Calculate quartiles, find outliers, and create a box plot.

- Create a line plot and a scatter plot.

- Calculate correlation and regression.

- Submit your final analysis.

### Prepare the Data *(20 points)*

1. Run the provided package dependency and data imports, and then merge the mouse_metadata and study_results DataFrames into a single DataFrame.

> - *The datasets are merged into a single DataFrame. (6 points)*

2. Display the number of unique mice IDs in the data, and then check for any mouse ID with duplicate time points. Display the data associated with that mouse ID, and then create a new DataFrame where this data is removed. Use this cleaned DataFrame for the remaining steps.

> - *The number of mice are shown from the merged DataFrame. (2 points)*
> - *Each duplicate mice is found based on the Mouse ID and Timepoint. (6 points)*
> - *A clean DataFrame is created with the dropped duplicate mice. (4 points)*

3. Display the updated number of unique mice IDs.

> - *The number of mice are shown from the clean DataFrame. (2 points)*

### Generate Summary Statistics *(15 points)*

Create a DataFrame of summary statistics. Remember, there is more than one method to produce the results you're after, so the method you use is less important than the result.

> - *A new DataFrame is created with using the summary statistics. (5 points)*

Your summary statistics should include:

- A row for each drug regimen. These regimen names should be contained in the index column.

- A column for each of the following statistics: mean, median, variance, standard deviation, and SEM of the tumor volume.

> - *The mean of the tumor volume for each regimen is calculated using groupby. (2 points)*
> - *The media of the tumor volume for each regimen is calculated using groupby. (2 points)*
> - *The variance of the tumor volume for each regimen is calculated using groupby. (2 points)*
> - *The standard deviation of the tumor volume for each regimen is calculated using groupby. (2 points)*
> - *The SEM of the tumor volume for each regimen is calculated using groupby. (2 points)*


### Create Bar Charts and Pie Charts *(15 points)*

1. Generate two bar charts. Both charts should be identical and show the total total number of rows (Mouse ID/Timepoints) for each drug regimen throughout the study.

    - Create the first bar chart with the Pandas DataFrame.plot() method.

    > - *A bar plot showing the total number of timepoints for all mice tested for each drug regimen using Pandas is generated. (4.5 points)*

    - Create the second bar chart with Matplotlib's pyplot methods.

    > - *A bar plot showing the total number of timepoints for all mice tested for each drug regimen using pyplot is generated. (4.5 points)*

2. Generate two pie charts. Both charts should be identical and show the distribution of female versus male mice in the study.

    - Create the first pie chart with the Pandas DataFrame.plot() method.

    > - *A pie plot showing the distribution of female versus male mice using Pandas is generated. (3 points)*

    - Create the second pie chart with Matplotlib's pyplot methods.

    > - *A pie plot showing the distribution of female versus male mice using pyplot is generated. (3 points)*

### Calculate Quartiles, Find Outliers, and Create a Box Plot *(30 points)*

1. Calculate the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin.

> - *A DataFrame that has the last timepoint for each mouse ID is created using groupby. (5 points)*
> - *The index of the DataFrame is reset. (2 points)*

2. Then, calculate the quartiles and IQR, and determine if there are any potential outliers across all four treatment regimens. Use the following substeps:

    - Create a grouped DataFrame that shows the last (greatest) time point for each mouse. Merge this grouped DataFrame with the original cleaned DataFrame.

    > - *Retrieve the maximum timepoint for each mouse. (2 points)*

    - Create a list that holds the treatment names as well as a second, empty list to hold the tumor volume data.

    > - *The four treatment groups, Capomulin, Ramicane, Infubinol, and Ceftamin, are put in a list. (3 points)*
    > - *An empty list is created to fill with tumor volume data. (3 points)*

    - Loop through each drug in the treatment list, locating the rows in the merged DataFrame that correspond to each treatment. Append the resulting final tumor volumes for each drug to the empty list.

    - Determine outliers by using the upper and lower bounds, and then print the results.

    > - *A for loop is used to display the interquartile range (IQR) and the outliers for each treatment group (10 points)*

3. Using Matplotlib, generate a box plot that shows the distribution of the final tumor volume for all the mice in each treatment group. Highlight any potential outliers in the plot by changing their color and style.

> - *A box plot is generated that shows the distribution of the final tumor volume for all the mice in each treatment group. (5 points)*

**hint:** All four box plots should be within the same figure. Use this Matplotlib documentation pageLinks to an external site. for help with changing the style of the outliers.

### Create a Line Plot and a Scatter Plot *(10 points)*

1. Select a single mouse that was treated with Capomulin, and generate a line plot of tumor volume versus time point for that mouse.

> - *A line plot is generated that shows the tumor volume vs. time point for one mouse treated with Capomulin. (5 points)*

2. Generate a scatter plot of mouse weight versus average observed tumor volume for the entire Capomulin treatment regimen.

> - *A scatter plot is generated that shows average tumor volume vs. mouse weight for the Capomulin regimen. (5 points)*

### Calculate Correlation and Regression *(10 points)*

1. Calculate the correlation coefficient and linear regression model between mouse weight and average observed tumor volume for the entire Capomulin treatment regimen.

2. Plot the linear regression model on top of the previous scatter plot.

> - *The correlation coefficient and linear regression model are calculated for mouse weight and average tumor volume for the Capomulin regimen. (10 points)*
