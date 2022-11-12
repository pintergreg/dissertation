---
title: "1. Introduction"
description: "Introduction"
date: 2022-07-07
draft: false
images: []
menu: 
  docs: 
    parent: "dissertation"
weight: 10
toc: true
---


## Background

Mobile phones are now fundamental parts of our life; they are practically always with us, wherever we go, almost as if they were a part of our body. The continuous communication between a device and the mobile networks leaves traces of our whereabouts in the operator's system. Via these devices, the mobile network can "sense" our movements, which is the basis of the "Smart City" concept [<a href="/docs/dissertation/bibliography#batty2012smart" title="M. Batty et al., “Smart cities of the future,” The European Physical Journal Special Topics, vol. 214, no. 1, pp. 481–518, 2012.">1</a>].

In the last few decades, anonymized Call Detail Records (<span class="acronym" title="Call Detail Record">CDR</span>) have become a common information source for analyzing the characteristics of human mobility. Numerous research has been published utilizing this source of data from all around the world, even from Hungary, e.g., [<a href="/docs/dissertation/bibliography#tettamanti2014mobile" title="T. Tettamanti and I. Varga, “Mobile phone location area based traffic flow estimation in urban road traffic,” Columbia International Publishing, Advances in Civil and Environmental Engineering, vol. 1, no. 1, pp. 1–15, 2014.">2</a>, <a href="/docs/dissertation/bibliography#egedy2021urban" title="T. Egedy and B. Ságvári, “Urban geographical patterns of the relationship between mobile communication, social networks and economic development–the case of Hungary,” Hungarian Geographical Bulletin, vol. 70, no. 2, pp. 129–148, 2021.">3</a>, <a href="/docs/dissertation/bibliography#szocska2021countrywide" title="M. Szocska et al., “Countrywide population movement monitoring using mobile devices generated (big) data during the COVID-19 crisis,” Scientific Reports, vol. 11, no. 1, pp. 1–9, 2021.">4</a>]. The research focuses on Budapest and its agglomeration. <span class="acronym" title="Call Detail Record">CDR</span>s contain the billed activities of the subscribers, providing information about the whereabouts of the population. Based on this massive information source, human mobility analysis is utilized in fields --- among others --- like social sensing, epidemiology, transportation engineering, urban planning, and sociology. Furthermore, the human sleep-wake cycle (<span class="acronym" title="sleep wake cycle">SWC</span>) is also studied by analyzing mobile phone network data.

The analysis of the human movement patterns based on the <span class="acronym" title="Call Detail Record">CDR</span> data, which makes it possible to examine a large population cost-effectively, resulted in several discoveries about human dynamics. These works usually consider the population as a homogeneous group, and the classification is based on some mobility indicators [<a href="/docs/dissertation/bibliography#pappalardo2015returners" title="L. Pappalardo, F. Simini, S. Rinzivillo, D. Pedreschi, F. Giannotti, and A.-L. Barabási, “Returners and explorers dichotomy in human mobility,” Nature communications, vol. 6, p. 8166, 2015.">5</a>]. The next step was adding external data sources to the mobile network data, extending the investigation to other population characteristics. Often, this external source is used to classify the data (e.g., by gender) and to analyze the classes using the previously introduced mobility indicators. Among others: social network data [<a href="/docs/dissertation/bibliography#cecaj2014re" title="A. Cecaj, M. Mamei, and N. Bicocchi, “Re-identification of anonymized CDR datasets using social network data,” in 2014 IEEE International Conference on Pervasive Computing and Communication Workshops (PERCOM WORKSHOPS), 2014, pp. 237–242.">6</a>], transportation data [<a href="/docs/dissertation/bibliography#huang2018modeling" title="Z. Huang et al., “Modeling real-time human mobility based on mobile phone and transportation data fusion,” Transportation research part C: emerging technologies, vol. 96, pp. 251–269, 2018.">7</a>], taxi trips [<a href="/docs/dissertation/bibliography#furno2017fusing" title="A. Furno, N.-E. El Faouzi, M. Fiore, and R. Stanica, “Fusing GPS probe and mobile phone data for enhanced land-use detection,” in 2017 5th IEEE International Conference on Models and Technologies for Intelligent Transportation Systems (MT-ITS), 2017, pp. 693–698.">8</a>], socioeconomic indicators (income, education rate, unemployment rate and deprivation index) [<a href="/docs/dissertation/bibliography#pappalardo2015using" title="L. Pappalardo, D. Pedreschi, Z. Smoreda, and F. Giannotti, “Using big data to study the link between human mobility and socio-economic development,” in 2015 IEEE International Conference on Big Data (Big Data), 2015, pp. 871–878.">9</a>], sale price of residential properties [<a href="/docs/dissertation/bibliography#xu2018human" title="Y. Xu, A. Belyi, I. Bojic, and C. Ratti, “Human mobility and socioeconomic status: Analysis of Singapore and Boston,” Computers, Environment and Urban Systems, vol. 72, pp. 51–67, 2018.">10</a>].

A part of this work also fits into the trends, using housing prices as a socioeconomic indicator. Housing price, however, is an indirect indicator for the <span class="acronym" title="Social Economic Status">SES</span>, so a more direct indicator, the cellphone price, was also investigated. While Blumenstock et al. used the call history as a factor of socioeconomic status [<a href="/docs/dissertation/bibliography#blumenstock2015predicting" title="J. Blumenstock, G. Cadamuro, and R. On, “Predicting poverty and wealth from mobile phone metadata,” Science, vol. 350, no. 6264, pp. 1073–1076, 2015.">11</a>], Sultan et al. [<a href="/docs/dissertation/bibliography#sultan2015mobile" title="S. F. Sultan, H. Humayun, U. Nadeem, Z. K. Bhatti, and S. Khan, “Mobile phone price as a proxy for socio-economic indicators,” in Proceedings of the Seventh International Conference on Information and Communication Technologies and Development, 2015, pp. 1–4.">12</a>] applied mobile phone prices as a socioeconomic indicator and identified areas where more expensive phones appear more often. However, only manually collected phone prices were used, and the analysis was not performed on the subscriber level.

## Research Goals

The goal of my research was to develop a methodology and implement a data processing framework that can evaluate mobile network data. This framework should also be able to calculate mobility indicators and associate socioeconomic indicators with the subscribers. As the mobility patterns of the subscribers can be extracted from the <span class="acronym" title="Call Detail Record">CDR</span>, the people can be distinguished based on their mobility customs. One of the main goals was to find a correlation between mobility and socioeconomic status.

As the mobile network data does not contain information about the subscribers' income, the <span class="acronym" title="Call Detail Record">CDR</span>s were required to be enriched with other data sources. My research focused on an indirect and a more direct feature in this regard. The indirect is the housing prices because the level of a neighborhood is used to infer the <span class="acronym" title="Social Economic Status">SES</span>. When the home location of a subscriber is known, the typical housing price of that area can be associated with the subscriber. Considering if someone lives in a more expensive area, their socioeconomic status should be higher, as well.

A more direct feature would be the price of the subscriber's cellphone. As the actual purchase price of a mobile phone can depend on several factors, the age of the device may be used in line with the recommended retail price.

Another goal was to analyze the commuting tendencies of the capital and its agglomeration. Kiss et al. state that although commuting is an essential and common phenomenon, its measurement is occasional and inadequate [<a href="/docs/dissertation/bibliography#kiss2015ingazas" title="A. Kiss and Z. Matyusz, “Az ingázás, mint forgalomkeltő tényező,” Munkaügyi szemle, vol. 59, no. 5, pp. 20–34, 2015.">13</a>]. Commuting is predominantly analyzed by the census, but that is performed only once in a decade; thus cannot follow sudden but permanent changes. They also stress that commuting should be examined frequently, and its methodology should be established [<a href="/docs/dissertation/bibliography#kiss2015ingazas" title="A. Kiss and Z. Matyusz, “Az ingázás, mint forgalomkeltő tényező,” Munkaügyi szemle, vol. 59, no. 5, pp. 20–34, 2015.">13</a>].

As questioning the population is a slow, tedious and expensive task, it would be obvious to automate the process with the available info-communication technologies (<span class="acronym" title="information and communication technology">ICT</span>). In this research, the application of <span class="acronym" title="Call Detail Record">CDR</span> processing was presented to examine commuting, mainly to Budapest, and the findings were validated by the results of studies that analyzed commuting using census.

Economic models distinguish city parts such as residential areas, industrial areas, business districts, and so on, but that is a relatively static, slowly evolving city layer. Mobile phone network data has the potential to describe the city structure via the inhabitants' mobility patterns. The next part of this research focuses on the effect of the <span class="acronym" title="sleep wake cycle">SWC</span> on the city structure. In this regard, it continued the commuting analysis, but the city structure was analyzed by the circadian rhythm of the people who live and work in a given area of Budapest.

Is it possible to cluster city areas by the time when the activity of the inhabitants, the workers, or the passers-by starts their activity in the morning or halts in the evening? Do city parts have "chronotypes"? Is there a structural or socioeconomic connection between the areas with the same "chronotype"? Can neighborhoods or districts be described by the terms "morningness" or "eveningness"? Another goal of this research was to answer these questions.

## Meso-data

Is this work dealing with Big Data? No, not really, as one of the V's of Big Data [<a href="/docs/dissertation/bibliography#mcafee2012big" title="A. McAfee, E. Brynjolfsson, T. H. Davenport, D. J. Patil, and D. Barton, “Big data: the management revolution,” Harvard business review, vol. 90, no. 10, pp. 60–68, 2012.">14</a>], volume, does not apply here. Historical data has been processed for a limited area (the capital and its agglomeration) and a limited period (one month). Increasing the observation area and period would increase the volume of the data. However, a year of data for the whole country should still be effortlessly manageable with the current set of tools that are not extraordinary.

Could it be Big Data? Yes, it could, if, for example, the analytics should be updated in real-time or almost real-time, so the velocity would be an issue. Some current analyses could even take an hour or two, though there could be plenty of room for optimization in my queries and scripts.

What is it, if not Big Data? I like the term "meso-data" (and "meso-computing") that Matt Williams proposed in his essay [<a href="/docs/dissertation/bibliography#williams2020meso" title="M. Williams, “Meso-computing and meso-data: the forgotten middle,” milliams.com. Aug. 28, 2020. Available: https://milliams.com/posts/2020/mesocomputing/">15</a>] to describe the processing challenges of the order of magnitude of this data.

## Data Science is like Origami

Origami[^1] is the art of paper folding, where after a specific sequence of simple folding steps, a sheet of paper becomes a figurine of an animal or an object. Data science is like origami, as during the data processing, simple steps are applied one after another while it starts to shape and new information is born. As everyone has a sheet of paper, everyone has a pile of data nowadays.


<figure id="">
<img src="paper-crane.png" alt="Paper crane by Caro Asercion, CC BY 3.0">
<figcaption><strong>Figure 1.1.:</strong> Paper crane by Caro Asercion, CC BY 3.0</figcaption>
</figure>



The question is, who can fold that data into art?

[^1]: In the Japanese word, origami, *ori* means "folding", and *kami* means "paper" ("ka" changes to "ga" in the compound word).
