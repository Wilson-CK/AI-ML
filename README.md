# AI-ML
Practical Application Assignment: Will the Customer Accept the Coupon? 
**Deliverables:**
Your final product should be a brief report that highlights the differences between customers who did and did not accept the coupons. To explore the data, you will utilize your knowledge of plotting, statistical summaries, and visualization using Python. You will publish your findings in a public facing GitHub repository as your first portfolio piece.
Github repository: https://github.com/Wilson-CK/AI-ML
Containing this Readme, Jupyter notebook, and original data files. 
** Summary of findings:**
** Original Dataframe**
Original dataframe “data” has:  12,684 rows and 26 columns.
Proportion of entries that accepted the coupon: 56.84%
** [Discovery]**  We can see that Coffee House makes up the most coupon category given, followed by cheap restaurants, carry out and bar, with expensive restaurants being the coupon type having the least number.
**[Discovery]**  Most coupons were given out during warmer temperature (80F) conditions, followed by moderate (55F), with cooler temperature (30F) being the least.
** Bar Coupons **
Bar dataframe “BarDF” has: 2,017 rows and 25 columns.
Proportion of entries that accepted the bar coupon: 41.00%
Acceptance rate of those who went to a bar 3 or fewer times a month: 37.06%
Acceptance rate of those who went to a bar more than 3 times a month: 76.88%
**[Discovery]** There is a much higher propensity for people who visit a bar greater than 3 times monthly to accept a bar coupon than those who only go to a bar 3 or fewer times per month.
Acceptance rate of those who went to a bar more than once a month and over age 25: 69.52%
Acceptance rate of those who went to a bar once or less a month and over age 25: 26.10%
Acceptance rate of those who went to a bar more than once a month and under age 25: 67.05%
Acceptance rate of those who went to a bar once or less a month and under age 25: 39.45%
**[Discovery]** People who go to the bar more frequently have a much higher likelihood of accepting a bar coupon than those who do not.  On the contrary, age (over vs under 25) only has a minor impact to their acceptance rate
Acceptance rate of those who went to a bar more than once a month, had passengers that were not a kid, and had occupations other than farming, fishing, or forestry: 71.79%
Acceptance rate of those who went to a bar more than once a month, had passengers that were kids, and had occupations other than farming, fishing, or forestry: 37.78%
Acceptance rate of those who went to a bar more than once a month, had no passengers, and had occupations other than farming, fishing, or forestry: 71.07%
**[Discovery]** Drivers who travel alone or have adult passengers have a much higher propensity of accepting a bar coupon thanF those who travel with kids as passengers.
Acceptance rate of those who went to a bar more than once a month, had passengers that were not a kid, and were not widowed: 71.79%
Acceptance rate of those who went to a bar more than once a month and were under 30: 72.17%
Acceptance rate of those who went to cheap restaurants > 4 times a month with income < 50K: 45.35%
**[Discovery]** Drivers who travel with adult passengers and visit the bar more than once a month have a high propensity of accepting a bar coupon.  Furthermore, people with lower income who frequently visit cheap restaurants tend not to accept the bar coupon.  
**[Hypothesis]** Drivers who travel alone or with adult passengers and visit the bar at least once a month have a much higher propensity of accepting a bar coupon than those who travel with kids or rarely visit the bar.
**Independent investigation: Carryout & Takeaway Coupons**
I chose the Carryout & Takeaway coupon group for this exercise.¶
Carryout & Takeaway dataframe “carryDF”:  has 2,393 rows and 25 columns
Proportion of entries that accepted the Carryout & Takeaway coupon: 73.55%
**Weather Factor:** Let's explore if and how weather plays a part in influencing people's coupon acceptance behavior, using a Seaborn countplot:¶

From the bar plot, it appears that Sunny weather has a strong influence towards people's Carryout & Takeaway coupon acceptance rate. However, it's not clear what the actual acceptance to refusal ratio is.¶
Let's determine the acceptance to refusal ratio for each weather category:
Coupon acceptance         No	Yes          ratio
weather                     
Rainy    			124   	195  	1.572581
Snowy     		90   	217  	2.411111
Sunny   		 	419  	1348  	3.217184
 **[Discovery]** Here we can definitively see that Sunny weather has the strongest influence to coupon acceptance rate, followed by Snowy and Rainy weather.
 **Driving Destination Factor:** Next, let's explore if and how the driving destination plays a part in influencing people's coupon acceptance behavior, using a Seaborn countplot:
It appears that home and no urgent place have the strongest factors to people's coupon acceptance rate, followed by work.
Now, let's map out the coupon acceptance to rejection ratio:
Coupon acceptance         No	Yes          ratio
destination                        
Home             		138 	 515  	3.731884
No Urgent Place  	232  	746  	3.215517
Work             263  499  1.897338
**[Discovery]** Here we can clearly see that the home as the driving destination has the strongest acceptance ratio than no urgent place and work.
**Gender Factor:** Let's explore if and how gender plays a part in influencing people's coupon acceptance behavior, using a Seaborn countplot:
**[Discovery]** From the plot, both female and male genders have relatively similar coupon acceptance rate and acceptance-to-rejection ratio. So I concluded that gender does not play a notable role in the coupon acceptance rate.
**Coupon Expiration Factor:** Let's check to see if and how coupon expiration plays a part in influencing people's coupon acceptance behavior, using a Seaborn countplot:
From the plot, we can see that the longer expiration of 1-day has a much higher acceptance rate than that of a 2-hour expiration.
# Now, let's map out the coupon acceptance to rejection ratio:
Coupon acceptance         No	Yes          ratio
expiration                     
1d          		318  	1138  	3.578616
2h          		315   	622  	1.974603
**[Discovery]” Here we clearly see that the 1-day coupon expiration has a higher acceptance ratio than the 2-hour counterpart.
**Time of Day Factor:** Let's explore if and how time of day plays a part in influencing people's coupon acceptance behavior, using a Seaborn countplot:
At a glance, we can see that 2pm and 6pm appear to have the highest coupon acceptance ratio.
Next, let's determine the coupon acceptance to rejection ratio:
Coupon acceptance         No	Yes          ratio
time                    
10AM  			154  	363  	2.357143
10PM  			111  	350 	3.153153
2PM    			29  	189  	6.517241
6PM    			76  	359  	4.723684
7AM   			263  	499  	1.897338
**[Discovery]** From the graph, we can confirm that 2pm has the highest coupon acceptance ratio and 7am has the lowest.
**Any Passenger(s) Factor:** Finally, let's check to see if and how any passenger(s) plays a part in influencing people's coupon acceptance behavior, using a Seaborn countplot:
From the graph, it appears driving with friend(s) has the strongest coupon acceptance rate.

Next, let's determine the coupon acceptance to rejection ratio:
Coupon acceptance         No	Yes          ratio
passanger                     
Alone      		383  	1022  	2.668407
Friend(s)  		179   	560  	3.128492
Kid(s)      		45   	107  	2.377778
Partner     		26    	71  	2.730769
**[Discovery]** From the plot, we can confirm that driving with friend(s) has the highest propensity of accepting a coupon.  In contrast, driving with kid(s) has the lowest acceptance ratio.
**[Hypothesis]** Drivers who are driving back home or to non urgent destinations with friends or partner during sunny weather in the afternoon and given a Carryout and Takeaway coupon with 1 day expiration have a very high propensity of accepting it. In contrast, those who are driving to work with kids on a rainy day in the morning and given the same coupon that expires in 2 hours have very low likelihood of accepting it.¶
** [Next Steps & Recommendations]** More analysis can be performed on other coupon types such as those for coffee houses and cheap/expensive restaurants. Additionally, we can check out more categorical relationships such as the correlation among marital status, occupation, any children, income and educational levels to the acceptance rate of various coupon types.
For the bar coupons, I would advise Amazon to target drivers who travel alone or with adult passengers and visit the bar at least once a month. Additionally, extend their coupon expiration to 1 day as opposed to 2 hours to provide more flexibility - as opposed to sense of urgency - for the drivers to choose.
For the Carryout & Takeaway coupons, I would recommend Amazon to focus on drivers who are driving back home or to non urgent destinations with friends or partner during sunny weather in the afternoon and, as above, extend the coupon expiration to 1 day as opposed to 2 hours.

