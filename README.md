# Identifying the Nature of Chinese Influence in the AIIB

Established in January 2016, The Asian Infrastructure Investment Bank (AIIB) is a Chinese-proposed and led multilateral development bank with the stated aim of filling Asia's infrastructure gap. As of September 2024, the Bank boasts 110 member states and has made $45 billion in total lending.  

Since its inception, however, some [think tanks](https://www.brookings.edu/wp-content/uploads/2017/04/chinas-emerging-institutional-statecraft.pdf) and [commentators](https://www.csis.org/analysis/what-do-asian-infrastructure-investment-banks-recent-forays-outside-asia-mean) have warned that the AIIB may not serve as a neutral investment bank focused on lending to countries that are the most in need, but as a Chinese foreign policy instrument to promote its influence abroad. The fact that China possesses an oversized, 26% of the AIIB's vote share, the AIIB headquarters being located in China, and that it has always had a Chinese president suggest that China may have sufficient influence over how the Bank lends.  

A central argument is that the AIIB allows China to fund countries multilaterally rather than bilaterally, which would invite less scrutiny while promoting China's international image as an institutional player. That is, whereas excessive bilateral economic flow to countries already in China's orbit could lead to accusations that it is buying political influence, such criticisms are much less likely to occur if the funding is delivered multilaterally through the AIIB. Another possibility is that China directs AIIB loans to countries where it is politically difficult to implement its own state-led bilateral initiatives. For example, for countries such as the Philippines and India with which China has territory disputes, funding infrastructure development through AIIB loans may be more convenient than investments from Chinese state-owned enterprises or official loans. It is worth noting that the two frameworks point to opposite relationships between AIIB lending and China's state-led, bilateral efforts to improve relations. The first implies that AIIB lending would flow to countries with which China is already attempting to improve relationships, while the second suggests that the two will be negatively correlated.

This project empirically examines the extent to which China influences AIIB lending to align with its foreign policy interests. Given the ongoing geopolitical competition between China and the United States, any potential expansion of Chinese influence deserves careful attention. More broadly, evidence pointing to Chinese influence in AIIB lending could signal challenges to the norms of the international development lending regime by foregrounding great power politics over need-based loan allocation.

## Unit and Time of Analysis
It is important to first establish the population of states that are plausible recipients of AIIB loans. While all AIIB members are potential recipients, developed countries such as Germany and South Korea are highly unlikely to receive loans. Consequently, I consider plausible recipients as all developing members of the AIIB and those who have received a loan. Countries in this list enter into the observation starting from the year they first joined the AIIB. The entire period of the analysis runs from 2016 to 2022. 

The dataset is in panel structure. There are 58 unique countries and 309 country years. See the figure below for an illustration of how many countries in the observation joined the AIIB each year. 

![fig1](maps%20and%20graphs/countries_joining.png)

## Variables
I obtained the number and amount of AIIB loans by project from the official website [official website](https://www.aiib.org/en/projects/list/index.html). I operationalize the dependent variable in three ways: the total loan volume per country year, the total project count per country year, and a binary indicator reflecting whether a country received any AIIB loans in a given year.

I use three variables to proxy for China's official bilateral initiatives: [Chinese state loans](https://www.aiddata.org/data/aiddatas-global-chinese-development-finance-dataset-version-3-0), [foreign direct investment (FDI)](https://www.aei.org/china-global-investment-tracker/?ncid=txtlnkusaolp00000618) by Chinese state-owned enterprises (SOE), and [foreign visits](https://link.springer.com/article/10.1007/s11558-022-09459-z#Fn6) by the Chinese President/Premier. Since official loans are issued by the Chinese government, their allocation and amounts are likely indicative of the Chinese leadership's intent to strengthen relationships with specific countries. The same logic applies to FDI by state-owned enterprises since they are under the direct control of Chinese officials. Finally, Chinese leaders are likely to visit countries with whom they would like to improve bilateral relations. There is no instance of multiple visits by Chinese leaders to a single country in the same year, meaning that the variable is binary. 

The figures below demonstrate the aggregated allocation of AIIB loans, Chinese loans, Chinese SOE FDI, and the destination of leadership visits. 

![fig2](maps%20and%20graphs/aiib_loan.png)

![fig3](maps%20and%20graphs/china_loan.png)
There does not appear to be much overlap between AIIB loans and Chinese official loans. While AIIB loans tend to concentrate in Southeast and South Asia, Chinese loans flow predominantly to Central Asian countries.

![fig3](maps%20and%20graphs/china_fdi.png)

![fig4](maps%20and%20graphs/china_visit.png)

There is somewhat of a bigger overlap between AIIB loans and the other two key IVs, although the relationship is not very clear.

I include the following controls: Whether a country is in the Belt and Road Initiative (BRI), GDP per capita, corruption level, regulatory quality level, World Bank (WB) and Asian Development Bank (ADB) loan volume, and forecasted infrastructure investment needs as a percentage of GDP. I obtained values for forecasted infrastructure investment from the G20's [Global Infrastructure Outlook](https://outlook.gihub.org). Since the estimates do not cover all the countries in my dataset, I impute missing values with the averaged values of three countries that have the most similar GDP per capita. 

## Regression Output 
I estimate three models: fixed effects ols to examine if Chinese foreign policy interests affect AIIB loan volume, fixed effects logit to examine if Chinese foreign policy interests affect the probability that a country receives an AIIB loan in a year, and fixed effects negative binomial to examine if Chinese foreign policy interests affect the the number of AIIB loans countries receive. Year dummies are included in all models, and a trend term is also present for fixed effects OLS. I estimated a model for each of the three key variables of interest with the same controls and subsequently concatenated their point estimates and confidence interval into one figure. Results for the control variables come from the regression featuring logged Chinese loans as the key IV. Robust standard errors are applied in all models.

![fig5](Regression%20output/fixed_effects_ols.png)
The result suggests that out of the three proxies for official Chinese attempts to enhance bilateral ties, logged FDI is the only one whose coefficient is statistically significant. The effect size may not be substantively meaningful, however, as the model suggests that a 1% increase in FDI volume from Chinese SOEs in the previous year only leads to a 0.122% decrease in the amount of AIIB loan a country receives this year. The negative relationship supports the reasoning that China directs AIIB loans to locations where it is politically infeasible for its state enterprises to invest bilateraly . In addition, a 1% increase in the amount of ADB and WB loans received reduces a country's AIIB loans by 0.2%. This makes sense economically, as countries that have received more loans from other development banks in the previous year would not need as much lending from the AIIB.

![fig6](Regression%20output/fixed_effects_logit.png)
Although there are no statistically significant coefficients at the 5% level in the logit model, both the coefficients of logged SOE FDI and logged ADB and WB loan volume have p-values very close to 0.05. This suggests that both more Chinese FDI and more loans from the two development banks reduces the probability of a country receiving an AIIB loan.

![fig7](Regression%20output/fixed_effects_nb.png)
The only variable with a statistically significant coefficient here is corruption. Contrary to common sense, a one-unit increase in the level of corruption is associated with a 7.37-fold increase in the number of AIIB projects. when interpreted in standard deviation terms, becoming one standard deviation more corrupt is associated with a 2-fold increase in the number of AIIB projects. Previous research [suggests](https://www.sciencedirect.com/science/article/abs/pii/S109095161000074X) that Chinese FDI disproportionately flows more to countries with poor institutions, so it is not entirely surprising that AIIB loans may exhibit the same behavior. Still, more research needs to be done to examine this relationship. 

## Summary Remarks
The above analysis provides some evidence of China strategically exercising its influence in AIIB lending to advance its interests abroad. Specifically, countries that receive more FDI both receive less AIIB loans on average and have a reduced probability of receiving any AIIB loans in a year. As opposed to complementing its existing efforts, China appears to be directing AIIB loans to locations where it is not making inroads to improve relations through official means. Consequently, Chinese influence in the AIIB may be best characterized as leveraging the institution to fund infrastructure projects in countries that are challenging for bilateral funding.
