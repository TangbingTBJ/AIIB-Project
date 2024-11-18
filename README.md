# AIIB Project

Established in January 2016, The Asian Infrastructure Investment Bank (AIIB) is a Chinese-proposed and led multilateral development bank with the stated aim of filling Asia's infrastructure gap. As of September 2024, the Bank boasts 110 member states and has made $45 billion in total lending.  

Since its inception, however, some think tanks and commentators have warned that the AIIB serves not as a neutral investment bank focused on lending to countries that are the most in need, but as a Chinese foreign policy instrument to promote its influence abroad (see [here](https://www.brookings.edu/wp-content/uploads/2017/04/chinas-emerging-institutional-statecraft.pdf) and [here](https://www.csis.org/analysis/what-do-asian-infrastructure-investment-banks-recent-forays-outside-asia-mean)). One of the central arguments is that the AIIB allows China to carry out its strategic lendings multilaterally rather than bilaterally, which would invite less scrutiny while promoting China's international image as an insitutional player. The fact that China possesses an oversized, 26% of the AIIB's vote share, the AIIB headquarter being located in China, and that it has always had a Chinese president suggest that China has sufficient leverage over how the Bank lends. 

This project aims to empirically examine this claim to see if these claims conform to reality. Given the ongoing geopolitical competition between China and the United States, any potential expansion of Chinese influence deserves careful attention. More broadly, evidence pointing to Chinese influence in AIIB lending could signal challenges to the norms of the international development lending regime by foregrounding great power politics over need-based loan allocation.

## Unit and Time of Analysis
It is important to first establish the population of states who are plausible recipients of AIIB loans. While all members are technically potentially recipients, the AIIB is highly unlikely to lend to developed countries such as Germany and South Korea. Consequently, I consider plausible receipients as all developing members of the AIIB and those who have received a loan. Countries in this list enter into the observation starting from the year they first joined the AIIB. The entire analysis runs from 2016 to 2023. 

The dataset is in panel structure. There are 58 unique countries and 421 country years. See the figure below for an illustration of how many countries in the observation joined the AIIB each year. 

![fig1](maps%20and%20graphs/countries_joining.png)

## Variables
The dependent variable is the volume of AIIB loans in millions USD. It is derived by collecting the number of projects and their respective values from the AIIB's [official website](https://www.aiib.org/en/projects/list/index.html) and then aggregating by country year.

I use three variables to proxy for Chinese foreign policy interests: [Chinese state loans](https://www.aiddata.org/data/aiddatas-global-chinese-development-finance-dataset-version-3-0) (millions USD), [foreign direct investment (FDI)](https://www.aei.org/china-global-investment-tracker/?ncid=txtlnkusaolp00000618) by Chinese state-owned enterprises (S0E) (millions USD), and [foreign visits](https://link.springer.com/article/10.1007/s11558-022-09459-z#Fn6) by the Chinese president/premier. Since official loans are issued by the Chinese government, their allocation and amounts are likely indicative of the Chinese leadership's intent to strengthen relationships with specific countries. The same logic applies to FDI by state-owned enterprises since they are under the direct control of Chinese officials. Finally, Chinese leaders are likely to visit countries with whom they would like to improve relationship with. There is no instance of multiple visits by Chinese leaders to a single country in the same year, meaning that the visit variable is essentially a binary one. 

The figures below demonstrate the aggregated allocation of AIIB loans, Chinese loans, Chinese SOE FDI, as well as the destination of leadership visits.

![fig2](maps%20and%20graphs/aiib_loan.png)

![fig3](maps%20and%20graphs/china_loan.png)
There does not appear to be much overlap between AIIB loans and Chinese official loans. While AIIB loans tend to concentrate in Southeast and South Asia, Chinese loans flow predominantly to Central Asian countrires

![fig3](maps%20and%20graphs/china_fdi.png)

![fig4](maps%20and%20graphs/china_visit.png)

There appears to be somewhat of a bigger overlap between AIIB loans, SOE FDI volume, and leadership visits, although the relationship is not very clear.

I include the following standard controls: GDP, GDP per capita, corruption level, regulatory quality level, infrastructure quality, and World Bank and Asian Development Bank loans. While politically relevant variables such as whether a country is in the Belt and Road Initiative and foreign policy alignment with China could theoretically affect AIIB loan allocation, I decide keep the model succint and only include them if I find a statistically significant relationship between my key IVs and AIIB loan. 

## Regression Output 

