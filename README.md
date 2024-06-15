# Data Analysis Singapore Rainfall

## Executive Summary

This analysis investigates the impact of weather elements such as rain, sunshine, and temperature on agricultural yield and production in Singapore. The goal is to enhance water efficiency, reduce wastage, and improve crop productivity for sustainable farming practices. Through heatmap and correlation observations, it is evident that humidity and rainfall negatively correlate with agricultural production, indicating the importance of spotting trends in humidity levels. On the other hand, minimum average temperature has a positive correlation with agricultural production, emphasizing the significance of colder weather. Stable average temperatures over three decades allow farmers to select crops best suited for the temperature range of 27.8 to 28.8 degrees Celsius, ensuring consistent growth and cost savings on supporting infrastructures. Further advancements using machine learning algorithms will enable accurate prediction of rainfall frequency and magnitude, leading to a more effective decision support system for farmers. The analysis also suggests omitting the number of raindays variable, as it shows the weakest correlation to agricultural production.

---

## Problem Statement

Using information on elements of weather for example and not limited to rain, sunshine, temperature. In order to analysis if there is a measurable impact on the yield and production of agricultural products like livestock and vegetables. This will lead to improved water efficiency, reduced water wastage, and increased crop productivity, ultimately benefiting the agriculture industry and ensuring sustainable farming practices in Singapore.

---

## Datasets

1. [**Agriculture, Animal Production and Fisheries**] : Total count livestock slaughtered per year [Source](https://www.singstat.gov.sg/publications/reference/ebook/industry/agriculture-animal-production-and-fisheries)
1. [**Agriculture, Animal Production and Fisheries cont.**]: Weight of local production per year [Source](https://www.singstat.gov.sg/publications/reference/ebook/industry/agriculture-animal-production-and-fisheries)
1. [**rainfall-monthly-number-of-rain-days**] : Average number of rainy days per month [Source](https://www.singstat.gov.sg/publications/reference/ebook/society/environment)
1. [**rainfall-monthly-total**] : Average number of rainfall per month [Source](https://www.singstat.gov.sg/publications/reference/ebook/society/environment)
1. [**relative-humidity-monthly-mean**]: Average monthly humidity [Source](https://www.singstat.gov.sg/publications/reference/ebook/society/environment)
1. [**sunshine-duration-monthly-mean-daily-duration**]: Average daily sunshine hours per month [Source](https://www.singstat.gov.sg/publications/reference/ebook/society/environment)
1. [**monthly-air-temperature-and-sunshine-relative-humidity-and-rainfall**] : Average daily surface air temperature per year [Source](https://www.singstat.gov.sg/publications/reference/ebook/society/environment)
---

## Data Dictionary

|Features|Type|Dataset|Description|
|---|---|---|---|
|**year**|*integer*|all data source|Year of data captured.| 
|**average_rainfall**|*float*|rainfall-monthly-total.csv|Average monthly rainfall in respective year|
|**average_raindays**|*integer*|rainfall-monthly-number-of-rain-days.csv|Average monthly days of rain in respective year| 
|**average_humidity**|*float*|relative-humidity-monthly-mean.csv|Average monthly humidity in respective year| 
|**average_daily_sunshine(hrs)**|*float*|sunshine-duration-monthly-mean-daily-duration.csv|Average hours of sunshine per day in a month for respective year| 
|**mean-air-temperature-daily-maximum(°C)**|*float*|monthly-air-temperature-and-sunshine-relative-humidity-and-rainfall.csv|Average daily maximum temperature for respective year| 
|**mean-air-temperature-daily-minimum(°C)**|*float*|monthly-air-temperature-and-sunshine-relative-humidity-and-rainfall.csv|Average daily minimum temperature for respective year| 
|**mean-avg-air-temperature-absolute-extremes-maximum(°C)**|*float*|monthly-air-temperature-and-sunshine-relative-humidity-and-rainfall.csv|Average monthly absolute extreme maximum temperature for respective year| 
|**mean-avg-air-temperature-absolute-extremes-minimum(°C)**|*float*|monthly-air-temperature-and-sunshine-relative-humidity-and-rainfall.csv|Average monthly absolute extreme minimum temperature for respective year| 
|**poultry_produced**|*integer*|agriculture-production.csv|Total number of all poultry produced, not only limiting to chickens and ducks, in respective year| 
|**chickens_produced**|*integer*|agriculture-production.csv|Total number of chickens produced in respective year| 
|**ducks_produced**|*integer*|agriculture-production.csv|Total number of ducks produced in respective year| 
|**vegetables_produced(tonnes)**|*integer*|agriculture-production-cont.csv|Total number of vegetables (tonnes) produced in respective year| 


---

## Summary of Analysis

The correlation analysis reveals interesting insights regarding the relationship between weather factors and agricultural production. Both rainfall and humidity exhibit weak negative correlations (-0.15) with poultry and vegetable production, indicating limited influence. Conversely, the minimum average temperature demonstrates moderate positive correlations (0.48 for poultry and 0.63 for vegetables), suggesting a stronger association with agricultural output. However, extreme cold temperatures show minimal correlations (0.1 for poultry and 0.25 for vegetables). 

The bimodal or multimodal distribution of average rainfall indicates unpredictable weather patterns, potentially affecting agricultural outcomes. Box and whisker plots show consistent weather data with low variability, while poultry and vegetable production exhibit more variability. An outlier is observed in vegetable production between 1995 and 2000 do not align with the observed weather-related correlations, warranting further investigation. Overall, these findings emphasize the varying impacts of weather factors on agricultural production, with minimum average temperature playing a more significant role compared to rainfall and humidity.

Average temperature shows minimal fluctuations, around a range of approximately 1 degree Celsius over three decades. This stability allows farmers to select crops that thrive best within the temperature range of roughly 27.8 to 28.8 degrees Celsius. Consequently, they can maintain farming specific crops without the need for frequent changes. Moreover, consistant temperature implies that supporting infrastructures for these crops can be utilized long term, fostering cost-effective investment in the necessary infrastructure to support crops that are well-suited to flourish within this stable temperature range.

---

## Conclusions

For the agriculture industry, weather plays an important part in the effectiveness of production. Through this analysis, we are able to observe that there is a correlation between weather and agriculture production. Seasons with increased humidity is likely to correlate with decreased agriculture production puting more emphasis on the importance of spoting trends of humidity. This analysis also provides observations of the correlation between weather and agricultural production in Singapore by providing a picture of historical trends on the effect. Through this analysis, a stronger correlation of colder temperature but not to the extreme end was found, with the consideration that rainfall and raindays have an effect in weather.

Average temperature shows minimal fluctuations, around a range of approximately 1 degree Celsius over three decades. This stability allows farmers to select crops that thrive best within the temperature range of roughly 27.8 to 28.8 degrees Celsius.

---

## Limitations and Recommendations

As average temperature remain relatively constant thoughout 30 years, as analysied above, we recomend that farmer select crops that thrive best within the temperature range of roughly 27.8 to 28.8 degrees Celsius as it allows them to reliably grow crops and save cost with minimal need to change supporting infrastructures for these crops

Further models will be necessary to accurately predict frequency and magnitude of rainfall to better offer an effective decision support system that can provide timely recommendations to farmers. This entails utilizing advanced data analysis techniques, like machine learning algorithms, to analyze historical rainfall patterns and identify influential factors. By leveraging these techniques, we can improve the precision of trend analysis, leading to more reliable predictions of future rainfall patterns. This enhanced system will provide farmers with precise information to adjust accordingly and have measures in place with the predictions, improving agricultural productivity and sustainability in Singapore.

With the insights gain from this analysis, perhaps future analysis may consider omitting the number of raindays variable as it has shown to have the weakest correlations to agricultural production.