# arms-embargoes-effectiveness-DA-proj5
SP21 Decision Analytics Mini Project 5

## Background 
This project aims to investigate the legal flow of weapons and the effectiveness of arms embargoes from 1960 - 2020 in reducing military expenditure. Arms embargoes are a type of sanction that can be used to coerce states and non-governmental actors to improve their behavior in the interests of international peace and security, according to the definition from [SIPRI Arms embargoes](https://www.sipri.org/databases/embargoes). Arms embargoes are one of the most frequently used types of economic sanctions but they are perceived as one of the least effective, and there are researches on the state's compliance with arms embarges like [this](https://journals.sagepub.com/doi/abs/10.1177/0022343312470472). 

In particular, I want to investigate the effectiveness of arms embargoes in different countries by comparing the trend of the count of embargoes and the trend of military expenditure (in Million USD). The assumption here is that an effective embargo will cause military expenditure to decrease. 

The military dataset I used for this study is from the [Stockholm International Peace Research Institution ](https://www.sipri.org/), which is an international institute based in Stockholm. It was founded in 1966 and provides data, analysis, and recommendations for armed conflict, military expenditure, and arms trade as well as disarmament and arms control. 


## Business Question 
_1. In general, are arms embargoes effective in reducing world military expenditure?_


## Data Question 
_1. Is the change in number of arms embargoes positively or negatively related to change in world military expenditure_


## List of Data Source 
I obtain my data source from [Stockholm International Peace Research Institution ](https://www.sipri.org/), and [United Nations Department of Economics and Social Affiars](https://population.un.org/wpp/Download/Standard/CSV/) And attached are links to my source cvs files: 
- [SIPRI Arms embargo archive data](https://github.com/sophiaxuu/arms-embargoes-effectiveness-DA-proj5/blob/main/embargo.csv) that contains information on all multilateral arms embargoes that have been implemented by an international organization, such as the EU or UN, or by a group of nations.
- [SIPRI Military Expenditure Database](https://github.com/sophiaxuu/arms-embargoes-effectiveness-DA-proj5/blob/main/military-exp-m-usd.csv). This is data for military expenditure by country in current US$ (millions), presented according to calendar year, for 173 countries for the period 1960-2020. 
- [World Population by Country in 2020](https://github.com/sophiaxuu/arms-embargoes-effectiveness-DA-proj5/blob/main/population2020.csv). 


## Data Analysis & Visulization 
### Clusters of countries based on military expenditure and count of trade embargoes
![Figure4](https://github.com/sophiaxuu/arms-embargoes-effectiveness-DA-proj5/blob/main/figure4.png)
First, we look at the overview landscape of arms embargoes that are imposed from 1960 to 2020. Here is a bubble plot of different countries with expenditure on the x-axis and count of embargoes on the y-axis, and population size as the size of the bubble. We can see that except for China (the big red dot on the right), most of countries that receive arms embargo has a relatively small population. There are one cluster of countries here receive one embargo, another cluster of those receiving two, and two exceptions of Ethiopia receiving three and Afghanistan receiving four. 


### To answer the question of: Is the change in number of arms embargoes positively or negatively related to change in world military expenditure? 
We can take a look at this figure1: 
![Figure 1: Number of arms embargo and military expenditure trend 1960-2020](https://github.com/sophiaxuu/arms-embargoes-effectiveness-DA-proj5/blob/main/figure1.png)
In this figure, the histogram shows the count of arms embargoes worldwide over time, and the lines shows the military expenditure change overtime for different countries. Overall, we can see a reverse relationship between number of embargoes and military expenditure. Overall, we can see a reverse relationship between number of embargoes and military expenditure. Except for a few countries like China (yellow line) that increases their military expenditure significantly from 10 Billion USD to 250 Billion USD, the military expenditure of most countries are stable over time. 

### Interesting findings 
Notice here that in above figure1, the yellow (China) has exceptionally high growth rate from 1990 to 2020, with average military expenditure of 10K Million USD to 250K Million USD, which align with the high growth rate of China. Russia here also have significant increase in military expenditure. 

Next, we look at another figure2, which is figure1 except China and Russia so we can take a closer look at the rest of countires. 
![Fig2](https://github.com/sophiaxuu/arms-embargoes-effectiveness-DA-proj5/blob/main/fig2.png) 
To take a closer look, notice that for the yellow line (Iraq), every time there is a high count of the arms embargo, the military expenditure drop, and vice versa - indicating that Iraq's military expenditure is highly influenced by arms embargo.  Looking into the data, i find that none of the arms embargo is targeted directly to Iraq, but it indirectly has a significant impact. 

## Business Answer 
Our findings here show that trade embargoes, even if not directly targeted towards a country, is generally effective in reducing the worldwide military expenditure as shown in the inverse relationship between expenditure and count of embargoes. Some exception like China and Russia requires further analysis. Some countries like Iraq are more highly impacted by arms embargoes. 

With these findings, our targeted stakeholder of our analysis - The United Nations - could better decide if they want to impose an arms embargo based on its effectiveness on different countries.

# Data Analysis Steps Description 
Google Colaboratory notebook with analysis available here: [Open In Colab](https://colab.research.google.com/drive/1Mix73NaJx25IoKyW1owFaKrPeOkagu8O?usp=sharing)

1. Import Libraries 
2. Import datasets 
3. Use Groupby to get count of embargoes for each country 
4. Use Plotly Express histogram to graph the count of embargo grouped by countries over all years   
5. Merge arms embargo, military expenditure and population datasets
6. Plot Line Plot of Military Expenditure over 1960-2020
7. Combine two histogram and line plot to evaluate effects of Arms Embargo on Military Expenditure



