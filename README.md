# Baby Names Analysis Project
This project analyzes French, US, and British baby names data to explore trends in birth rates, particularly focusing on gender proportions over time. The analysis covers various data manipulation and visualization techniques using R programming language and popular libraries such as tidyverse, ggplot2, and plotly.

## Project Overview
The primary objectives of the project are:

- Gender Proportion Analysis: Calculate the proportion of female births over time and compare across different datasets (France, USA, and others).
- Popularity Trends: Analyze and plot the most popular names by year and gender.
- Visualization: Generate meaningful plots to visualize the trends in baby names popularity using R libraries (ggplot2, plotly).
- Rescaling Popularity Curves: Normalize name popularity curves so that the maximum popularity of each name is scaled to 1, allowing for easier comparison.
## Datasets
- French Baby Names: A dataset containing baby names from France.
- US Baby Names: A dataset containing baby names from the United States.
- British Baby Names: A dataset used for comparison, though much of the focus is on the first two datasets.
## Dependencies
This project requires the following R libraries:

- tidyverse: For data manipulation and cleaning.
- ggplot2: For data visualization.
- plotly: For creating interactive plots.
- dplyr: For data manipulation and summary functions.
- reshape2: For reshaping data for analysis.
## Install the necessary dependencies by running:

```R
install.packages(c("tidyverse", "ggplot2", "plotly", "dplyr", "reshape2"))
```
## Code Structure
The project is structured around several R scripts and code chunks:

- Proportion of Female Births: This code calculates and plots the proportion of female births by year across the different datasets.
- Popularity Trends: This section identifies the most popular names in each country and plots the popularity curves by gender.
- Offset Popularity Curves: Plot popularity trends offset by gender and country, showcasing the evolution of baby names over time.
- Rescaling Popularity Curves: All popularity curves are rescaled so that their maximum popularity equals 1, allowing for easier visual comparison.
## Usage
- Load the datasets (french_df, us_df, etc.) into R.
- Use the functions provided to process and manipulate the data.
- Visualize the results using the predefined ggplot and plotly functions.
## Example
To calculate the proportion of female births in the French dataset:

```R
calc_prop_female(french_df)
```
### To visualize the popularity trends:

```R
ggplot() +
  geom_line(data = calc_prop_female(french_df), aes(x = year, y = proportion_girls, color = "France")) +
  geom_line(data = calc_prop_female(us_df), aes(x = year, y = proportion_girls, color = "USA")) +
  labs(title="Proportion of Female Births by Country", x="Year", y="Proportion of Female Births") +
  scale_x_continuous(breaks = seq(1880, 2021, 5))
```
### Results and Observations
The proportion of female births has shown a decreasing trend over time, stabilizing around 50% in recent years.
Name popularity exhibits significant fluctuations, with certain names experiencing bursts of popularity in specific periods.
Rescaling popularity curves provides a clearer understanding of how names rise and fall in popularity relative to their peak.
