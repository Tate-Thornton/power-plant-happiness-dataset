

This document will look at a common societal metric for growth: infrastructure, and compares it with a question: is renewable energy a good investment? While there is much research detailing why renewable energy (nuclear, hydroelectric, geothermal, solar, and wind) power plants are good for the environment, a common defense is that they are expensive and cost too much to make. This document will examine the numbers and draw an insight into how the construction of renewable power plants affects various economic and wellbeing factors for the people who live in that same country.

# Data
Three datasets are being examined:
The World Resources Institute's Global Power Plant Database (https://datasets.wri.org/datasets/global-power-plant-database), available through the Creative Commons Attribution 4.0 License (https://creativecommons.org/licenses/by/4.0/). This dataset views grid-level power plants around the world, geo-locating them with additional information per plant, including generation, capacity, and fuel types.

The World Happiness Report's Figure 2.1 Dataset (https://www.worldhappiness.report/data-sharing/), which lists each country and gives them an aggregated Happiness score with a 95% confidence interval, with contributing factors also provided.

The World Bank's World Development Indicators Dataset (https://data.worldbank.org/country/1W), which contains a wealth of information for most countries in the world, including health, societal, economic, environmental, and institutional. 

# Process
First, some manipulations were made. To the Power Plant Dataset, a new column was added, "renewable" which checks each power plant's primary_fuel, returning a Yes if the primary_fuel is Solar, Hydroelectric, Wind, Biomass, Geothermal, and Wave or Tidal, and a No if it is Gas, Coal, Oil, Waste, Nuclear/Storage, Cogeneration, Petcoke, or Other. Some name mismatches between the different datasets were rectified (Russian Federation vs Russia, Republic of Korea vs Korea, etc.), as well as several countries present on the Power Plant database but not present on the World Bank database were dropped for clarity. 

Exploratory data analysis was performed, using a combination of SQL queries and some alternative views through Google Sheets. Another data manipulation compared the proportion (out of 1) of the total registered power plants were a county were renewable vs non-renewable (E.G., a country with only renewable plants would have a value of 1, and a country with only non-renewable plants would have a value of 0), and summed for each country.  This data series was then graphed against various factors from the World Bank dataset.

# Findings
The correlation between Gross GDP and Renewable Power Plant Proportion was not identifiable. There was a relatively even spread across the different proportions, with a few staggering outliers in GDP. In a similar vein, GDP Per Capita was also not directly conclusive. Most of the variables had a reasonable spread across the various proportions/countries, with a few outliers in each category. 

# Conclusion
Unfortunately, there is no statistically significant correlation between the Proportion of Renewable Power Plants against most other variables or metrics widely accepted as beneficial for country and population wellbeing. A guess as to why this is could take multiple forms:
1) Perhaps countries that have built their own renewable power plants versus those who had renewable power plants funded by wealthier nations would have some correlation. If a version of this dataset could be procured that listed the fund sources for the construction of each power plants (AKA foreign sources or domestic sources), perhaps a more holistic view of this subject could be attained.
2) It is possible that a more zoomed-in view would be more accurate, such breaking down the population statistics by region, city, or province and compare that to what type of power plants supplies the region. This could provide an alternative, more community-focused lens on the issue, although it would time-consuming and difficult to aqcuire all of the data to be fully repreentative.
3) It is also simply possible that there is no real correlation. Technology changes and evolves, but older technology is not always rendered obselete, and any economy that continues to function and serve its citizens is a good economy. Other factors, such as allocation of funds to research or energy sectors, education, and other high-level statistics would be much more representative of wellbeing statistics.

