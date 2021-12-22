# An Analysis of Kickstarter Campaigns

## Overview of Project

The purpose of this analysis is to explain to Louise how successful different kickstarter campaigns were based on multiple factors including goal amount, pledged amount, country origin, date, and entertainment categories/subcategories. We used this data to determine appropriate goal amount, start date of kickstarter, and the duration of the kickstarter.

## Analysis and Challenges

### For Theater Outcomes by Launch Date

- We used a pivot table where we filtered by Parent Category and Years, made our columns based on outcome, our rows by Date Created Conversion (Excel automatically inserted Years and Quarters, but we made sure to only have Date Created Conversion on rows), and values to count of Outcomes. We made this pivot chart to determine the best months to launch a kickstarter. We also made a line pivot chart to display the trends of the outcomes. Some of the challenges I faced was determining the axes of the pivot table. It definitely throws me off when the columns and values have the same variable. The other challenge I had was sorting the columns to show successful first.

### For Outcomes Based on Goals

- We created 12 goal amount ranges starting from less than $1,000 to over $50,000, by $5,000 increments, to count the number of successful, failed, and canceled kickstarters. We used the `COUNTIFS()` excel function with 3 criteria; the goal amount range, the outcome of the kickstarter, and the subcategory, which we filtered to plays only. We then added the total kickstarters for each range using the `SUM()` excel formula, and then gave a percentage for each outcome (successful, failed, and canceled) based on total projects. We then used this data to see what goal ranges were the most successful and which were the most failed ranges to give an estimate on how large the kickstarter goal should be. Some of the challenges I faced was getting the inequalities right in the `COUNTIFS()` formula. After correcting my formula, I also needed to use absolute	 references for my column ranges. This table took the longest to create as the formulas had to be exact and correct for all 36 cells (12 ranges, 3 outcomes). 

## Results

### What are two conclusions you can draw about the Theater Outcomes by Launch Date?

- My two conclusions are:

1) The month with the most successful kickstarters was May, followed by June, then July. Furthermore, The end of spring is the best time to launch a kickstarter, and is not recommended to launch one after the end of summer.

2) When you filter out the months May through July, The two lines follow the same trend, meaning that the ratio between successful and failed kickstarter is almost the same. The lines peak and valley at the same time.

### What can you conclude about the Outcomes based on Goals?

- My conclusion is that lower goal amounts tend to be more successful than goals with a high goal amount. A goal amount in the $0 - $9,999 amount have more successful kickstarter than it does failed kickstarters. Another goal range that had more successful kickstarters than failed was the $35,000 - $44,999 range, however, there is not enough data to back up that theory. 

### What are some limitations of this dataset?

It is difficult to determine why a kickstarter was successful based on the data. Questions that need to be asked are:

1) How were the kickstarters advertised? How much was spent on advertising?

2) We have amount pledged and number of backers, and the only number we can get from the two is average pledged per backer. How do we know if the average wasn't skewed by some outlier, say one millionaire funded 50% of the kickstarter?

### What are some other possible tables and/or graphs that we could create?

Just by looking at the dataset, Spotlight and Percentage Funded are almost positively correlated. It almost looks like if the kickstarter had a spotlight, then the kickstarter would more than likely be fully funded, or close to fully funded. I can see the correlation thanks to the conditional formatting on the Percentage Funded column. If we conditionally formatted the spotlight to where true is blue and false is red, the two columns would almost look identical.

![Spotlight_True](Users/joseperez/Desktop/Spotlight_PercentFunded.png)