# What measures improve living standards while keeping CO2 emissions in check?
Analyzing the effect that different quality of life metrics have on human development (HDI), and per capita CO2 emissions


Context:
In today’s world, climate change is starting to have a massive effect on many developing countries already, and global temperatures are rapidly increasing. However, many countries are still quite poor and need to develop, but this comes with the side effect of increased CO2 emissions. As a result, an important question to ask centers around how countries can easily improve their quality of life while minimizing CO2 emissions. While embracing clean energy can certainly help, there are still concrete development goals that countries can aim for to get the best out of public policy making

Data Structure Overview:
In order to answer the question, I decided to use human development index (HDI) as the dependent variable for living standards, and consumption based CO2 emissions per capita (in tons) for the measurement of CO2 emissions. These two metrics are widely available from 1990-2022 (the years of my analysis), and this means that they can be used for a long term examination of how certain development goals can affect quality of life and carbon emissions.

For the controls, I used access to drinking water and sanitation services, access to DTP and Hepatitis B vaccines, and per capita calorie supply for health indicators. For education quality, I used primary school enrollment and expected years of schooling. Additionally, I included access to electricity because it was one of the great innovations of the 20th century, and greatly revolutionized societies around the world, and is essential for weighing how an increased reliance on energy can affect quality of life.

I used excel to clean the data and SQL to join the different files together, and I performed a regression on jupyter notebooks.

Summary:
The data in question showed that most of the independent variables had a significant and positive effect on HDI, a significant and negative effect on GDP per capita, and some controls had a statistically significant positive effect on CO2 emissions, some a negative effect, and some an insignificant effect.

The policy goal that I would recommend the most from the analysis is measures to increase enrollment in school, and most importantly, increase the amount of years that people spend in school, especially because of the fact that many developing countries are set to see significant increases in their population. As a result, easing access to school, and making schooling preferable to working jobs at a young age is a goal that can lead to countries developing more easily, and increasing the ability of countries to produce green energy sources that can accommodate increased consumption without major increases in greenhouse gas emissions. Additionally, as the regression for CO2 emissions shows, an increase in education does not lead to a significant increase in emissions.

Deep Dive:
When it comes to improving human quality of life, all else equal, a higher GDP per capita isn’t as consequential as it may seem, as $1 in GDP per capita at PPP only translates to 1.43*10-6 additional units of HDI, and even at a scale like $10,000, that figure is only 0.0143 units (with the scale being between 0 and 1), which is a very small difference. The coefficient is significant at the alpha=0.001 level, but the actual coefficient is pretty small.

Additionally, a calorie consumption diet that’s 1,000 calories higher on average will only increase a country’s HDI by 0.005 units, while increases in vaccination also don’t seem to have substantial effects on HDI on their own.

However, what can be seen from the results is that education is highly impactful on human development (as it forms ⅓ of HDI), with each additional year of schooling adding more to HDI than $10,000 to a country’s GDP per capita, all else equal.
Enacting policies aimed at extending education to at least 12-14 years, or even up to 16 could have a massive effect on quality of life for many countries. This is especially important because of the fact that developing countries are going to have far more children than other countries, and those children are going to be the future of the country, meaning that higher quality education for them will lead to more human capital development.
However, in order to prevent a brain drain, this would require fixes for the labor market, making it easier to effectively utilize the education one obtains, with jobs in green energy certainly being a possibility for many people.

It’s clear that access to clean drinking water and sanitation was more important than vaccinations in this analysis, however, it’s important to note that with respect to the health based metrics in question, some are starting to approach universal access, far higher than in the 1990s.
From 2020-2022, the first quartile of country year combinations for access to clean drinking water was equal to roughly 86%, for sanitation, it was closer to 67%, for the two vaccinations, it was near 80%. What this means is that most countries already have significant access to these public health measures, and increased access, while not extremely expensive, will likely not increase living standards as much as other development goals. However, due to the potentially low costs, it’s likely still a worthwhile investment.

Part of the reason why so many control variables may’ve had a negative effect on GDP per capita may’ve been that the bulk of the data for many of the variables converged around 1 (representing the share of the population), and as a result, many countries with low GDP numbers may’ve still had high values for some of the explanatory variables.

Recommendations:
Ultimately, a recommendation that I would have for the countries is to focus more on developing green energy and electrical grids powered by green energy sources, because essentially every country could have more green energy and as a result, they could have the ability to improve their standard of living without increasing their emissions too much. Additionally, this would be a great opportunity for countries to create jobs for their citizens, especially those with access to higher education, and it would be a great opportunity for developed countries to reindustrialize.

However, in that event, I believe that we should see much more concerted efforts at producing more green energy sources, and finding cheaper innovations, all throughout the world, be it through state directed action, public private partnerships, or subsidies for green energy providers, and companies that meet goals centered around shifts to green energy. Additionally, I believe that developed countries should limit tariffs on green energy imports, and also guarantee cheap access to green energy for developing countries, provided developing countries approve.
Developing countries could also clearly benefit from making a goal to increase access to education, especially with the emerging opportunity to utilize that education in order to help enhance productivity in green energy sectors.

Limitations:
One limitation is that as a result of the fact that I analyzed data from 1990-2022, many of the metrics that measured quality of life, such as access to vaccines, sanitation and water facilities, and electricity have started to become more and more readily adopted, meaning that countries that are still very poor are poor due to reasons going beyond just a lack of access. This may mean that the quality of the services that the countries have may be more important than simply having the services, meaning that in a modern context, simply having access isn’t enough.

Another issue may’ve come from the fact that one of the two main vaccines I used had an insignificant effect on quality of life, which I find hard to believe. It may be that I should’ve looked at more vaccines in order to more confidently determine whether vaccines as a category significantly impact quality of life, which I still believe they do.

Another issue with this sort of analysis is that you can’t just target some of the goals like increasing GDP and expect to hit them, the way you can with increasing access to vaccines, or even electricity. Additionally, even if you hit educational targets, you still need to have a labor market that offers enough jobs for the educated workforce, otherwise, you can become a victim of the brain drain.

Lastly, while you can perform a regression analysis, you cannot truly hold all else equal, because aiming to increase access to electricity will invariably lead to a higher GDP. As a result, I believe the model showing how certain variables affect GDP is flawed, and likely suffers from methodological issues.

#Data Sources for the Project

References:
Consumption-based CO₂ emissions per capita vs. GDP per capita. Our World in Data. (2024). https://ourworldindata.org/grapher/consumption-co2-per-capita-vs-gdppc 
Consumption-based CO₂ emissions per capita vs. human development index. Our World in Data. (2024). https://ourworldindata.org/grapher/per-capita-co-emissions-vs-human-development-index
Daily supply of calories per person. Our World in Data. (2024). https://ourworldindata.org/grapher/daily-per-capita-caloric-supply
Expected years of schooling. Our World in Data. (2025). https://ourworldindata.org/grapher/expected-years-of-schooling 
Share of population using at least a basic drinking water source. Our World in Data. (2024). https://ourworldindata.org/grapher/population-using-at-least-basic-drinking-water
Share of the population using at least basic sanitation services. Our World in Data. (2024). https://ourworldindata.org/grapher/share-of-population-with-improved-sanitation-faciltities
Share of the population with access to electricity. Our World in Data. (2025, January 24). https://ourworldindata.org/grapher/share-of-the-population-with-access-to-electricity
Total net enrolment rate in primary education. Our World in Data. (2025). https://ourworldindata.org/grapher/total-net-enrollment-rate-in-primary-education
Vanderslott, S., Dattani, S., Spooner, F., & Roser, M. (2024, February). Vaccination. Our World in Data. https://ourworldindata.org/vaccination
