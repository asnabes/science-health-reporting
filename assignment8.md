# <div align="center">Assignment 8</div>
I’m in Michigan, where Ford and General Motors are headquartered. I was inspired by Randy’s example story pitch about Northwestern employees, and I decided to compare how much General Motors and Ford employees have given to Sen. Gary Peters, D-Mich., and how much they have given to his Republican opponent, John James. James earned $19,067.91 from GM and Ford employees from June 1, 2019 to March 31, 2020, while Peters earned $21,372 in that same period. I used this time period because James announced he was running against Peters in [June 2019](https://www.detroitnews.com/story/news/politics/2019/06/05/john-james-site-senate-run/1357289001/). James had earned money before that date, but I wanted to start my comparison around the time he started his campaign.

I plan to calculate the number of employees at Ford and GM who gave to each candidate (which Randy also did in his example). I also plan to interview a few Ford or GM employees who donated to Peters and a few who donated to James. I also hope to talk to a political scientist who knows about who Michigan auto company employees have voted for historically. I would spend about a week on this story.

I conducted this analysis of the data:
1. On the FEC website, I found the people who donated to Peters and James who work at Ford or GM. I searched for “Ford Motor Company”, “General Motors”, “GM” and “Ford.” I downloaded the two datasets. I gave the files new names in Excel. 
2. I uploaded the two datasets to R. 
3. There were a lot of columns in the two CSV files that weren’t helpful, so I created two new dataframes with the columns I wanted to keep.<br />
Here is the code I wrote:<br />
newpeters <- peters[,c(18,19,20,21,24,25,27,28,35,36)]<br />
newjames <- james[,c(18,19,20,21,24,25,27,28,35,36)]
4. Some of the people listed in the datasets did not actually work at Ford or GM. They worked at places that had “Ford” or “GM” in their name, like Henry Ford Health System. I deleted these people from the two files in Excel.
5. In R, I found the sum of all the rows in the “contribution_receipt_amount” column for both dataframes (which Randy also did).<br />
Here is the code I used:<br />
sum(newjames$contribution_receipt_amount)<br />
sum(newpeters$contribution_receipt_amount)

Headline: Ford and GM employees gave slightly more to Sen. Gary Peters than to John James from June 2019 to March 2020

Nutgraph:<br />
         Peters is running for re-election against James, who lost to Sen. Debbie Stabenow, D-Mich., in 2018. James announced that he would face Peters in [early June in 2019](https://www.usnews.com/news/politics/articles/2019-06-06/james-announces-senate-run-against-sen-peters-in-michigan), according to the Associated Press. According to [Bridge Magazine](https://www.bridgemi.com/economy/ten-things-might-surprise-you-about-michigans-economy), manufacturing is the second largest part of the economy in the Detroit area, with Ford and GM headquartered in the area. Who are Ford and GM employees supporting in this year’s Senate election? Employees from the two companies gave Peters $21,372 from June 2019 to the end of this March, while James earned only about $2,300 less than Peters — $19,067.91.
