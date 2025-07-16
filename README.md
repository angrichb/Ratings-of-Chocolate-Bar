# cocoa-insights

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


### Distribution of Chocolate Bar Ratings

<img width="2400" height="1800" alt="histogram_chocolate_ratings" src="https://github.com/user-attachments/assets/d817b0a2-8619-4606-b383-f6e059d9fe9b" />
Interpretation: This histogram shows the distribution of expert ratings for chocolate bars. The ratings primarily fall between 3.0 and 4.0, with the most common rating being 3.5. The distribution is approximately symmetric, though there is a slight concentration of ratings just below the peak. Very high ratings (above 4.5) and very low ratings (below 2.5) are rare, suggesting that most chocolate bars receive moderate evaluations with few outliers.

### Cocoa Percentage vs. Rating

<img width="2400" height="1800" alt="scatter_cocoa_vs_rating" src="https://github.com/user-attachments/assets/17b578d8-c115-4fd1-99e1-65e973aa4da2" />
Interpretation: This scatterplot shows the relationship between the cocoa percentage in a chocolate bar and its expert rating. Overall, there is no strong linear relationship between the two variables. Ratings appear to be most concentrated between 60% and 80% cocoa, where a wide range of scores from 2.5 to 4.0 are observed. Extremely high cocoa percentages (above 90%) do not consistently receive higher or lower ratings, suggesting that cocoa content alone is not a reliable predictor of perceived quality. This implies that other factors, such as flavor balance, texture, or bean origin, may play a more significant role in expert evaluations.

### Cocoa % vs. Rating (Top Countries)

<img width="3000" height="2400" alt="facet_scatter_cocoa_vs_rating_by_country" src="https://github.com/user-attachments/assets/f11c0e71-98a4-4d80-8018-0c8fd0abb8d1" />
Interpretation: This faceted scatterplot explores the relationship between cocoa percentage and expert rating across the top six chocolate-producing countries. While none of the countries show a clear linear correlation, some distinct patterns emerge:

* In the U.S., a wide range of ratings is observed across a broad cocoa percentage range (60%–90%), suggesting a diverse product portfolio with varied quality outcomes.
* Countries like France, Canada, and the U.K. show moderate clustering around cocoa percentages of 70–75%, with most ratings falling between 3.0 and 4.0.
* Italy and Ecuador exhibit tighter clustering, implying more consistency in both cocoa content and ratings.

Overall, the plots suggest that the relationship between cocoa content and expert rating varies by country, and no consistent trend indicates that higher cocoa content guarantees higher ratings. This supports the idea that chocolate quality is influenced by multiple factors beyond just cocoa percentage, including origin, processing, and recipe style.

### Dashboard using Tableau 

<img width="619" height="477" alt="Screenshot 2025-07-14 at 8 10 52 PM" src="https://github.com/user-attachments/assets/6e9cf5e9-f509-45ee-8c4e-aa943253d9b7" />

Interpretation: This dashboard summarizes key insights from the chocolate bar ratings dataset. The average rating by company location reveals that certain countries, such as the U.S. and Canada, consistently produce higher-rated chocolate bars. The histogram shows that ratings are concentrated between 3.0 and 4.0, suggesting that most chocolates receive moderate to high expert scores.
The scatterplot of cocoa percentage versus rating indicates no strong linear trend, though most products fall between 60% and 80% cocoa content. This suggests that higher cocoa content alone does not predict higher quality ratings.
Together, the visuals provide a comprehensive view of how chocolate bar ratings vary by geography, cocoa content, and overall distribution. This offers valuable insights for product comparison and quality benchmarking.


#### Business Practice Interpretation

This project integrates visual analysis using R and Tableau to explore patterns in expert chocolate bar ratings. By analyzing rating distributions, cocoa content, company locations, and bean origins, the project supports business decisions in product development, quality benchmarking, and strategic sourcing. The interactive Tableau dashboard allows for deeper exploration of these relationships and provides an accessible summary of the key findings. 


#### Limitations & Possible Extensions

One limitation of this project is the lack of information on sample sizes per company, which could affect the reliability of average ratings. The dataset also includes only a single review score per bar, without consumer data or sensory details. Additionally, while cocoa percentage is included, other factors that influence quality (e.g., bean origin, processing methods) are only partially captured. If extended, this project could include sentiment analysis of written reviews, predictive modeling of ratings based on bean origin and manufacturing country, or integration with sales and pricing data to explore value perception alongside quality.
