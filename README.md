# Kickstarting with Excel

## Overview of Project
This project challenges Data Analytic students to clean up the way data is stored and to analyze the information based on multiple variables. In this example we were to analyze information regarding fundraising goals and visualize raw numbers into clean, readable charts.

### Purpose
The purpose of my analysis was to correlate success criteria for campaigns based on what time of year Theater campaigns were launched and to break down "successful" outcomes based on the the fund rasing goal.  

## Analysis and Challenges
To measure outcomes based on Launch date, I had to convert the date information so I could cleanly pivot out the data by month. To do this, I created another column and used the formula ==(L2/86400)+DATE(1970,1,1) to get the date in the format of (MM,DD,YY).  I then had to create another column to filter out the data by Years.  To pull the years from the newly converted dates, I used the code =TEXT(J2,"YYYY").  From there I pivoted out the data with filters by Parenty Catergory and Years, and sorted by most successful months.

![Theater Outcomes based on launch date](https://user-images.githubusercontent.com/107078763/173841071-209c242e-ad98-40a0-a26d-bea071c01944.png)

To measure the outcomes based on goals, I created another sheet and measured the outcomes based on different ranges of goal money needed to be determined a successful campaign.  I had to use the COUNTIFS function because I needed the formula to measure a count if both criteria measures were met.  =COUNTIFS(Kickstarter!D:D,"<1000", Kickstarter!F:F,"successful")

  ![countifs](https://user-images.githubusercontent.com/107078763/176211348-88b7eb9a-f40a-4c0a-8240-7aa30aa0e6c3.png)


### Analysis of Outcomes Based on Launch Date
![](https://user-images.githubusercontent.com/107078763/173824774-eaa800f8-a599-4fd1-b544-321d4c3015aa.png)
This graph displays the number of successful, failed, and canceled Campaigns for the category of Theater based on when the campaign was launched.  The number of failed and canceled campaigns are fairly consistent across all months.  However, the months with the most successful campaigns are May through August.


### Analysis of Outcomes Based on Goals
![Countif](https://user-images.githubusercontent.com/107078763/176210931-1a925d76-1b68-478f-9206-e2825857519d.png)
This graph displays the successful, failed, and canceled outcomes as a percentage along with the goal of each campaign based on of how much money they were looking to raise.  
### Challenges and Difficulties Encountered
I struggled in the Analysis of Outcomes Based on Goals with having to recreate CountIf code.  It was tedious to have to edit 36 different CountIf statements because I was unable to use the same line for each cell.  I ended up using the same code from the number of successful outcomes and adjusting the statement based on the other two outcomes.
Another challenge I encountered was presenting this Analysis as a READ.md file.  I have never used this platform before so I had to use my Google-Fu skills to read and watch videos on how to successfully navigate this platform. I do see the benefit in the platform based on the structure is similar to coding platforms and will be useful when learning how to write HTML.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
1. The largest amount of successful campaigns were launched in summer months (May, June,July). 
2. December was the least successful month for Campaign launches.
- What can you conclude about the Outcomes based on Goals?
When the Goal amount was $10,000 or higher there was a less then 50% successful campaigns.
- What are some limitations of this dataset?
A limitation of this dataset is that the data is not very recent.  This data is from 2009 to 2017 so the most recent information is already 5 years old and would not help as much in 2022.
- What are some other possible tables and/or graphs that we could create?
  -Another way we could analyze this data would be to graph the correlation between successful outcomes and the number of backers for each campaign.  
  -We could also measure the outcomes based on how long the campaign was run by subtracting the time from launch date to the deadline to see if there was any     correlation between successful campaigns and failed based on how long each campaign was run.
