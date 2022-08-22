# TMBD Movie Data Analysis

The data set I've picked contains information about 10,000 movies collected from The Movie Database (TMDb), including user ratings and revenue. In this report, I'll be wrangling and analyzing the the tmdb data set.

The data set has two columns for budget and revenue. The second columns for each are the adjusted values in terms of 2010 dollars accounting for inflation over time.

The data set also has three columns with delimiters "|" that seperates various values.

Further description of the dataset and the questions I'll be answering are immediately after the first 5 code cell

I'll start the analyses by upgrading pandas then importing the required packages then reading the csv and checking out the overview of the data.

## Required Modules
* numpy
* pandas
* matplotlib.pyplot
* seaborn

## Installations
The modules listed in the section above can be downloaded in the anaconda IDE (recommended software to run the ipynb files) using `conda install module_name` or the conventional `pip install module_name`

## Setup
The recommended way to run the ipynb files is by setting up a virtual environment with conda and running the files in a jupyter notebook. Click [here](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html) to learn how to set up and manage virtual environments with conda.<br><br>
The html files that contains all the necessary codes and findings are also available in the `main` branch

## Known Bugs
The files in this repo currently have no bugs.

## Dataset Columns
1. id: This column won't be useful in the analysis as it's too specific to a movie and isn't a numerical data type that can be averaged out.
2. imdb_id: This column also won't be useful in the analysis as it's too specific to a movie and isn't a numerical data type that can be averaged out.
3. popularity: This column will be very useful in the analysis as it can be considered an independent variable for the revenue (dependent variable) as the revenue can depend on the popularity.
4. budget: The budget here isn't updated so I'll be using the adjusted budget
5. revenue: The revenue here isn't updated so I'll be using the adjusted revenue
6. original_title: This column also won't be useful in the analysis as it's too specific to a movie and isn't a numerical data type that can be averaged out.
7. cast: This column will probably be useful in the analysis.
8. homepage: This column also won't be useful in the analysis as it's too specific to a movie and isn't a numerical data type that can be averaged out.
9. director: This column will probably be useful in the analysis.
10. tagline: This column also won't be useful in the analysis as it's too specific to a movie and isn't a numerical data type that can be averaged out.
11. keywords: This column also won't be useful in the analysis as it's too specific to a movie and isn't a numerical data type that can be averaged out.
12. overview: This column also won't be useful in the analysis as it's too specific to a movie and isn't a numerical data type that can be averaged out.
13. runtime: This column will be very useful in the analysis as it can be considered an independent variable for the revenue (dependent variable) as the revenue can depend on the runtime.
14. genres: This column will probably be useful for the analysis.
15. production_companies: This column will probably be useful for the analysis.
16. release_date: This column also won't be useful in the analysis as it's too specific to a movie and isn't a numerical data type that can be averaged out.
17. vote_count: This column won't be useful as the average vote is giving us the required vote information and we don't need to know the amount of people that voted.
18. vote_average: This column will be very useful in the analysis as it can be considered an independent variable for the revenue (dependent variable) as the revenue can depend on the vote average.
19. release_year: This will be useful in the analysis to see the most-liked movies from year to year.
20. budget_adj: This is very important to the analysis as it can be considered an independent variable that the revenue generated can depend on
21. revenue_adj: This is probably the most important column here as most of this analysis will be based on it.

## Questions for Analysis
In this analysis, I'll be answering the following questions:
1. Which genres are most popualar from year to year
2. Properties associated with movies that have high revenues
- What level of popularity generates the highest revenue?
- How does runtime affect the revenue generated?
- How does vote average affect the revenue generated?
- How does budget affect the revenue generated?
- How does the genre affect the revenue generated?

## Method of Analysis
My analysis will start with data wrangling in which I'll be accessing the dataset and cleaning the errant data columns and rows.
After that, I'll be doing some exploratory data analysis to check out the trends the data has with scatter plots and bar charts.

## Summary of Findings
1. Thriller, Western, and War are the most popular genres year to year
2. Properties associated with movies that have high revenues include:
- High Level of popularity
- Long Runtimes
- High Vote Averages
- High Budget
