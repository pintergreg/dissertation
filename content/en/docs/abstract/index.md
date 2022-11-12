---
title: "Abstract"
description: "Abstract"
date: 2022-07-07
draft: false
images: []
menu: 
  docs: 
    parent: "dissertation"
weight: 2
toc: false
---


Mobile phones are now fundamental parts of our life; they are practically always with us, wherever we go, almost as if they were a part of our body. The continuous communication between a device and the mobile networks leaves traces of our whereabouts in the operator's system. In the last few decades, this information source has become a standard way of analyzing the characteristics of human mobility. During my research, I have analyzed Call Detail Records (<span class="acronym" title="Call Detail Record">CDR</span>), covering Budapest, Hungary, and the surrounding settlements. The goal of my research was to develop a methodology and implement a data processing framework that can evaluate mobile network data. This framework should also be able to calculate mobility indicators and associate socioeconomic indicators with the subscribers. As the mobility patterns of the subscribers can be extracted from the <span class="acronym" title="Call Detail Record">CDR</span>, the people can be distinguished based on their mobility customs. One of the main goals was to find a correlation between mobility and the socioeconomic status (<span class="acronym" title="Social Economic Status">SES</span>) and infer <span class="acronym" title="Social Economic Status">SES</span> from mobility.

Another goal was to analyze the commuting tendencies of the capital and its agglomeration. This objective required an algorithm to estimate the home and work locations of the subscribers. These two locations defined the direction of commuting. The further someone lives from their workplace, the longer the travel may last. Although several conditions affect the travel time, the time when people wake up can be a crucial indicator. The length of the workday is also connected to commuting. Mobile network data can be suitable for estimating these features.

I have utilized two features to characterize socioeconomic status, a direct and an indirect one. The indirect is the housing prices because the price-level of a neighborhood is used to infer the <span class="acronym" title="Social Economic Status">SES</span>. When the home location of a subscriber is known, the typical housing price of that area can be associated with the subscriber. Considering if someone lives in a more expensive area, their socioeconomic status should be higher. A more direct feature would be the price of the subscriber's cellphone, which can be associated with the subscriber, even though the actual purchase price can be affected by multiple factors. I introduced a new method to analyze the correlation between these socioeconomic features and the widely used mobility indicators.

Based on mobile network data, I found that the wealth level in Budapest has a certain influence on travel customs. The real estate price of home locations does not have a remarkable effect on the number of visited places (Entropy) and Gyration, which suggests that the travel diversity of the inhabitants is not strongly dependent on their socioeconomic status.

On the other hand, the mean distance between home and work locations is significantly correlated to property values. Living in a high-priced neighborhood in Budapest requires working in more expensive regions and vice versa. The people living in cheaper regions have to take longer routes to their work sites. This relationship can be explained by the fact that the less expensive districts are located at the perimeter of the city, while most of the workplaces are in the wealthier regions. Analyzing the residents' real estate values at home and work locations, I found a strong positive relationship.

I also demonstrated that the mobile phone price is an expressive socioeconomic indicator. It is capable of clustering the areas of a city and distinguishing the subscribers by mobility customs.

A new indicator, called wake-up time, is introduced to describe a behavior of a group of subscribers, and it denoted the time when this group starts to use the mobile network in the mornings. A negative correlation was found between wake-up time and mobility indicators (Entropy, Radius of Gyration): People wake up earlier and travel more on workdays. It is quite the contrary on holidays. A correlation has been identified between the wake-up time and the socioeconomic status using socioeconomic classes derived from housing prices and cellphone prices. The subscribers living in less expensive apartments get up earlier, and this tendency holds true in respect of the mobile phone prices, as well: subscribers who own more expensive cell phones tend to get up later.

An application of my research would be to support sociological studies using the anonymized mobile network data as a frequent, countrywide, and cost-effective alternative to the questionnaire-based methods like the census. These results may help further analyze the city structures, both functionally and sociodemographicly. The socioeconomic findings of this research can also contribute to a better understanding of the social structure of urban and rural environments if the analyses are performed at the country level. As city parts with early morning or late night activities may require different public transport services, the transportation infrastructure planning can also profit from this methodology. It could help urban development and --- based on international examples --- mobile network data can aid epidemic control. Business development could also benefit from the detailed insight of the neighborhood chronotypes, especially with the associated information on the home locations and the socioeconomic status of the subscribers.

