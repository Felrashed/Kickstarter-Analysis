# **Kickstarting with Excel: Analyzing Kickstarter Campaigns For Insights**

![](https://github.com/Felrashed/Kickstarter-Analysis/blob/main/Resources/Kickstarter_Banner.gif)

## **Overview of Project**

Our project goal was to collect, organize, and analyze available kickstarter fundraising data to identify and report on the characteristics of successful and unsuccessful (defined as "failed") campaigns to our project client, Louise. Furthermore, we aimed to simply convey this data using visualizations and dynamic data tables to offer both a digestable and interactive solution to the client.   
 
### **Purpose**

The analysis was commissioned by Louise, a playwright, with the aim of deriving actionable insights from available kickstarter campaign data and applying those insights towards optimizing a fundraising campaign for her theater production, *Fever.* Since she only has a budget of approximately $10,000, it was critical that our analysis achieved her desired outcomes. Specifically, these objectives were:
*   Determine if there are specific characteristics that make a campaign successful
*   Use insights to offer strategic approach to Fever fundraising initiatives
*   Gain understanding of the campaign lifecycle to mimic successful campaign       attributes
*   Determine the relationship between outcome, launch date, and funding goals
*   Visually represent campaign outcomes based on launch date and funding goals

## **Analysis and Challenges**

![](https://github.com/Felrashed/Kickstarter-Analysis/blob/main/Resources/workflow_analysis.png)

To achieve the desired outcomes I performed an analysis on a large kickstarter dataset including campaigns across multiple nations, categories, and with various funding goals. In order to accomplish this, the data first had to be cleaned and organized. This included steps to format Unix timecode into readable date formats, formatting campaign data to exclude blank entries, and applying filters alongside conditional formatting to present the data in a visually appealing and easy to read format. Additionally, I used the existing data to extract further insights, such as separating category and subcategory for a more detailed inspection of campaign performance using the "Text to Columns Wizard."

Text To Column Function Use Example:

![](https://github.com/Felrashed/Kickstarter-Analysis/blob/main/Resources/Text_to_Column.PNG)

Conditional Formatting Use Example:

![](https://github.com/Felrashed/Kickstarter-Analysis/blob/main/Resources/Conditional_Formatting.PNG)

Formula For Conversion From Epoch To Standard Date Format:

![](https://github.com/Felrashed/Kickstarter-Analysis/blob/main/Resources/Epoch_to_Standard.png)

Once the data was cleaned, organized, and filtered we were able to begin our analysis. The analytical process included creating descriptive statistics to find outliers and relationships in the data, pivot tables to easily visualize and compare data, and charts to help visualize trends and insights. 

Descriptive statistics used, accompanied by formulas:

![](https://github.com/Felrashed/Kickstarter-Analysis/blob/main/Resources/Descriptive_Stats.png)

Chart displaying outcomes of campaigns by parent category:

![](https://github.com/Felrashed/Kickstarter-Analysis/blob/main/Resources/Parent_Category_Outcomes.png)

Unfiltered Pivot Table Example:

![](https://github.com/Felrashed/Kickstarter-Analysis/blob/main/Resources/Pivot_Parent_Outcomes.PNG)

Two primary challenges in the data set were parsing out the category and subcategory data alongside the Unix timestamp conversion. While doing this by hand would have been a daunting task, I was able to use google to help me understand the Text to Column wizard to easily separate the subcategory from category in order to achieve more robust analysis. Similarly, I used this [website](https://www.epochconverter.com/) to confirm the presence of Unix Timestamp data and then applied the formulaic conversion displayed above afte gaining a better understanind of Unix Timestamp conversion from this [resource](https://websiteseochecker.com/blog/what-is-timestamp/) 

### **Analysis of Outcomes Based on Launch Date**

A review of the outcomes based on launch date reveals significant comparative data we can draw conclusions from. Primarily, Kickstarter campaigns for theater projects perform the best at achieving their fundraising goals when they are launched during late Spring through mid Summer. The months of April through July performed with the most successful outcomes, with May and June performing the best. While ascribing too much meaning may be a dubious endevour, it may be reasonable to conclude that since these months are traditionally associated with vacation, leisure, and recreational activities; backers are more willing to support campaigns during the season they are also able to derive [utility from them](https://en.wikipedia.org/wiki/Expected_utility_hypothesis)

Similarly, successful campaign performance begins to decline consistently as we exit the summer months and begin to approach the winter season, with the worst performing months being October through March. Based on these insights, we can conclude that the best time to launch a campaign is toward the very end of spring and toward the beginining of the Summer. Assuming historical trends hold, Louise's funding campaign will have the highest likelihood of success being launched during May and June. Furthermore, Louise should avoid launching any campaigns between the months of September and December. A line graph visualizing this trend data has been included for reference below:

![](https://github.com/Felrashed/Kickstarter-Analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals

A review of the goals data required that I formulate a table to represent the ranges of funding goals across all campaigns and then identify their associated success, failure, and cancellation rate. For this dataset, there were no cancelled projects, however we were able to gain considerable insight into the relationship between outcomes and the funding goals associated with the projects. This relationship is visualized alongside the tabular data used to create the chart for reference below:

[](https://github.com/Felrashed/Kickstarter-Analysis/blob/main/Resources/Outcomes_vs_Goals.png)


[](https://github.com/Felrashed/Kickstarter-Analysis/blob/main/Resources/Goals_Table.PNG)


By visualizing the data in tabular and chart form, I was able to offer the client, Louise, a direct view of the relationships between goals, outcome, and their rate of outcome. Doing so revealed that the data follows an irregular trend relationship between failed and successful outcomes as we progressed through various funding goal ranges. The most important insights were:
*   Campaigns had the greatest rate of success below $5,000
*   The failure rate of campaigns significantly increases as your goal sought exceeds $15,000 and continues until crossing over the $35,000 threshold
*   Campaigns with exceptionally large funding goals can be exceptions to the general trend, though the instances of success are few and far outweighed by failed campaigns suggesting there is more data required to understand why these campaigns were successful 

### **Challenges and Difficulties Encountered**

When working with new data, the initial challenge is always scrubbing the data and debugging. As previously stated, this involved learning new tools like the Text to Column Wizard, Unix Timestamp Conversion, and applying conditionally formated visualizations and conditional functions of analysis to parse out the correct data. With regard to the conclusions and analysis, there are limitations to the conclusions we can draw since the data only deals with kickstarter funding campaigns. Because of this limitation, we must assume our findings are not comprehensive since they lack consideration for funding campaigns and capital raised **outside** of kickstarter. 

Furthermore, budgeting and planning based on outcomes relative to funding goals and launch date has hinderences as well. There are too many external factors contributing to the success of a campaign, both quantitative and qualitative, to accurately derive actionable conclusions from outcomes relative to launch dates and funding goals. 

## **Results**

### **Conclusions Based on Launch Date:**

![](https://github.com/Felrashed/Kickstarter-Analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png)

**1.** The months of May and June are the most optimal time to launch a theater funding campaign on Kickstarter. Outside of these months, the success rate dwindles rapidly leading to the worst performing month, December. As previously stated, the association of the Summer months with recreation and entertainment is likely a contributing factor toward the success of theater campaigns during the same period. 

**2.** The rate of failure is relatively consistent throughout the year with a month-over-month uptick in failure only appearing during October. This suggests that while the rate of failure is consistent, the amount of failed campaigns is higher in the summer due to an overall greater volume of campaigns attempted. This likely explains the uptick in October as a final "push" of campaigns attempting to get funded outside of what is traditionally the most competitive months to launch. 

### **Conclusions Based on Goals:**

*   The ideal funding amount for a theater kickstarter campaign rests somewhere between $1,000 and $15,000 with the most optimal outcomes resting below the $5,000 threshold. While there are successful campaigns in excess of $15,000, the relationship between outcome and funding sought indicates that the highest likelihood of success for Louise's project requires her to maintain her target budget of $10,000 or less. For the purpose of this analysis, it is reasonable to conclude Louise's funding goal can be met, assuming she chooses to launch in the summer months and barring any external considerations (such as play quality, economic conditions, etc.) 

### **Limitations of this dataset:**

Some limitations in our data set include:
    **1.** The data is incomplete for our purpose. This dataset only represents kickstarter campaigns and is limited to a particular timeframe. To trully represent our conclusions better, we would want to factor in any funding campaigns launched **outside** of kickstarter. 
    **2.** The funding goals span a number of different countries and currencies. To accurately reflect the funding goal data, we would need to normalize the data into a single currency, for example USD, before we could truly understand the relationship between funding goals vs. outcomes.
    **3.** The date launched vs. outcomes analysis was certainly informative, but to accurately portray a relationship, it would be worthwile to note the duration of the campaign by factoring campaign end dates. Evaluating and comparing launch dates relative to number of days raising funds would likely yield more robust insights into when to launch a funding campaign as well as the optimal length of a campaign.   

### **What are some other possible tables and/or graphs that we could create?**

It would be helpful to view average contributions by backers alongside funding goals on a month over month view. This could potentially reveal that while certain months were best for launching, others would yield higher single contributions. This could be relevant when strategizing launch date relative to fundraising goal. For example: Though the summer months may be the best launch timeline, there could possibly be higher average contributions in months outside of this season. Assuming we were working with a smaller budget (~$2,500), it may be possible to achieve this by targeting a less competitive month with a lower target goal which could be more achievable than competing against a highly saturated theater funding campaign environment like the spring and summer. 
