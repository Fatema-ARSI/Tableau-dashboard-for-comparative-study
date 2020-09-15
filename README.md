# Tableau-dashboard-for-comparative-study-

## Project Objectve:

- Created a dashboard to do a comparative study on various parameters of different countries using the sample insurance dataset and world development indicators dataset.

## Dashboard:



 ## Dashboard Description
 
- A geographic map showing countries field. Colored the map based on Income column .

- Included a webpage to show data from world bank webpage driven by an url action from geography graph.

 - The country names in the map act as the trigger  https://data.worldbank.org/country/<country>?view=chart

- Created a KPI Table to show the comparison between the selected period and the prior period to the selected one.

- Created Growth Indicator Shapes based on the Growth %.

- Created a trend line to show the selected category values.

## Calculation fiel code:

- For categories [Parameter]:

CASE [CATEGORIES]

WHEN 'Life Insurance Share' THEN [Life insurance share]

WHEN 'Market Share' THEN [Market share > Total]

WHEN 'Penetration' THEN [Penetration > Total]

WHEN 'Ratio of Reinsurance Accepted' THEN [Ratio of reinsurance accepted > Total]

WHEN 'Retention Ratio' THEN [Retention ratio > Total]

END

- For Selected Period Value:

IF YEAR([Year])=[YEAR SECTION] THEN [categories calculation]

END

- For Comparison Period Value:

IF YEAR([Year])=[YEAR SECTION]-1 THEN [categories calculation]

END

- For Growth%:

ROUND(AVG([Selected Period Value]),4)-ROUND(AVG([Comparison Period Value]),4)

- For Growth Indicator

IF [Growth %]>0

THEN 'Positive'

ELSEIF [Growth %]=0

THEN 'No change'

ELSE 'Negative'

END

## Dashboard Link:

https://public.tableau.com/profile/fatema.arsiwala#!/?newProfile=&activeTab=0



 
