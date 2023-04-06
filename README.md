# Worldwide Energy Production and Consumption

## Purpose
The goal of this project was to investigate a correlation between GDP and an uptick in renewable energy production. To do this, we used a linear regression model to chart renewable energy consumption in quadrillion BTUs, against GDPs converted to the US Dollar. Our data on energy consumption was procured from the U.S. Energy Administration website, and our GDP info came from The World Bank's open data resource. 

## Questions to answer
How does GDP growth affect adoption/proliferation of alternative energies?

Which countries are leading the switch to alternative energies and who are the newest changes?

## Tools Used
Our data cleaning was mostly done via python in jupyter notebooks. Pandas covered the bulk of our work, with an honorable mention to fuzzywuzzy for a crucial fuzzy_merge. The database was setup in PostgreSQL via pgAdmin, and hosted through Amazon RDS. Actual analysis of our data was carried out using the linear_model from the scikitlearn library, and final visualizations were carried out via matplotlib and Tableau. 

## Results
There is definitely a correlation between GDP and growth/development of renewable energy production. We created two linear regression models, one for 2021 and one for 2011. The 2021 model had a higher accuracy score (70.6%) than the 2011 model (50.6%).
!(assets/images/2011 Renewables vs GDP.png)


## Dashboards
We produced several dashboards for our differnt datasets for readiblity reasons. 
## Production 
        https://public.tableau.com/app/profile/david.a.weissmann/viz/DUFinalProjectDavidW/Dashboard1?publish=yes
        It contains 2 charts the top shows who produced the most of a certain type of energy in 2021 and can be filtered based off the type of energy being produced. I           was suprised at how dominant the Chinese were in the Renewable energy sphere. The other is a breakdown of the different types of energy each country produces             over a series of years, and can be filtered based on the Country.
      
## GDP
        https://public.tableau.com/app/profile/matt.roberts6826/viz/GDP_16805755653810/Dashboard2
        This shows a breakdown of the change in GDP over time as well as the GDP of some of the smaller countries. It's interesting to see the rise of China in these             charts.
        
## Consumption
         https://public.tableau.com/app/profile/matt.roberts6826/viz/GDP_16805755653810/Dashboard2
         This shows the change in consumption over 4 decades for the largest consumers, the US, China, the Russian Federation, and The U.S.S.R. 

## Summary
There was added challenge in combining our datasets from different sources, particularly as it pertains to historic data going back to the last millenium. Countries that no longer exist (U.S.S.R., East/West Germany, etc.) were handled and input differently by each source. FuzzyWuzzy turned out to be an invaluable tool, allowing us to combine the datasets with minimal information loss. All in all, our model achieved a reasonable level of accuracy for the 2021 year, but we likely wouldn't recommend it be put up for commercial use. 
