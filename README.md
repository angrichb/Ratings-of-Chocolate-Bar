# Ratings-of-Chocolate-Bar

## Objective
The objective of my project is to explore factors that influence expert ratings of chocolate bars. By visualizing relationships between chocolate bar characteristics (such as cocoa percentage, bean origin, and company location) and their ratings, this analysis seeks to uncover trends that may inform product quality, sourcing decisions, and market positioning.

Key questions addressed include: 

* Are higher cocoa percentages associated with higher expert ratings? 
* Do certain regions or countries produce more highly rated chocolate? 
* Have chocolate bar ratings changed over time? 

By applying data visualization techniques to this dataset, the goal is to extract meaningful insights that could support strategic decisions in the specialty chocolate industry. 

## Data Source
Chocolate Bar Ratings dataset from Kaggel: https://www.kaggle.com/datasets/rtatman/chocolate-bar-ratings?resource=download. 

The dataset contains 1,795 observations of expert-rated chocolate bars evaluated by the website Flavors of Cacao. Each row in the dataset represents a single chocolate bar, and includes the following key variables:
* “Rating”: The expert rating on a scale from 1 to 5 (in 0.25 increments). 
* Cocoa_Percent: The percent cocoa content in the bar, expressed as a whole number.
* Company: The name of the manufacturer
* Company_Location: The country where the company is based.
* Bean_Origin: The specific region or country from which the cacao beans originated 
* Review_Date: The year in which the bar was reviewed
* Bean_Type: A description of the cacao bean variety 
* Broad_Bean_Origin: A more generalized bean origin

The data was imported into RStudio and cleaned to convert cocoa percentage from string format (e.g., “70%”) to numeric. Column names were simplified to improve usability during analysis. 

## Data Preparation
Minor cleaning steps were performed to ensure the data was ready for analysis:
* Column Renaming: Several variable names were simplified for readability and ease of coding. For example, “Company...Maker.if.known.” was renamed to “Company”, and “Cocoa.Percent” to “Cocoa_Percent”.
* Cocoa Percentage Conversion: The Cocoa_Percent column was originally stored as a character string with a percent symbol (e.g., "70%"). This symbol was removed and the values were converted to numeric so they could be used in continuous variable visualizations.
* Missing Data Check: A completeness check was performed, and no missing values were found across any columns.
* Variable Types: Variables were reviewed for appropriate data types. Rating and Cocoa_Percent were treated as continuous variables, while variables like Company_Location, Bean_Origin, and Bean_Type were used as categorical variables.

## Analysis
<img width="2400" height="1800" alt="top_chocolate_countries" src="https://github.com/user-attachments/assets/3354fb97-e56c-4296-9305-284856ccc810" />
Interpretation: Only countries that have 5 or more chocolate bars in the dataset are shown in the chart. In the full dataset, some countries only have 1 or 2 bars reviewed. Including them would clutter the plot and distract from meaningful comparisons. This bar chart shows the countries with the highest number of chocolate bars reviewed (5 or more). The United States stands out with a significantly higher number of bars compared to other countries, followed by France, Canada, and the U.K. This suggests a strong presence of chocolate manufacturers in these regions or greater participation in the review process. The chart highlights geographic concentration in chocolate production and visibility.
