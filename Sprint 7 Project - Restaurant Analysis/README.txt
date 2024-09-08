TripleTen Sprint 7 Project - Zomato Analysis
This is the last project I worked on in the TripleTen BI Analyst program. 

Restaurant Analysis
The project task was to figure out what factors make restaurants more popular and what contributes to higher rating of the restaurant

The Data
The dataset has the following columns:

'id' : unique restaurant ID
'name' : name of the restaurtant
'city' : the city where the restaurant is located
'rating' : the rating of the restaurant
'rating_count' : number of ratings the restaurant has
'cost' : average cost of the restaurant
'cuisine' : the type of cuisine the restaurant serves
'lic_no' : unique license number of the restaurant
'link' : link to the restaurants website
'address' : the address of the restaurant
'menu' : link to the restaurant's menu

The Process
1. Data Cleanoing
To find the accurate rating of each restaurant, I had to remove empty or incomplete data from the dataset using a calculated field to show a blank field that I filtered out when it came to the visualizations. When it came to the number of ratings for each restaurant, I clean up the data by removing “too few of ratings” from the data so that it wouldn’t mess with the data presentation since it wasn’t valid to the analysis. When looking at the average price at a restaurant, I filtered out prices that were greater than 1,000 as outliners and grouped them together. This way I can get the price closer to the average of 290. Also, prices above 1,000 were insignificant compared to the other prices since they made up less than 0.01% of all the other prices.
2. Visualizations
  a. Bar Graph - Overview of all the restaurants at different price groups and how many number of ratings those restaurants have.
  b. Scatterplot with trend line - Comparing all the restaurants between price v rating, we can see a trend where the average 	rating     	goes up as the price goes up. This means pricier restaurants tend to be of greater quality.
  c. Scatterplot with trend line - Restaurants that have more than 1000 number of ratings were grouped together to signify that 	they were among the most popular restaurants since the number of ratings is equal to foot traffic the restaurant gets. The 	average rating trend goes up even more among the popular restaurants as the price goes up
  d. Bar Graph - Looking at restaurants with more than 1000 number of ratings, we can see the most popular cuisines among those 	restaurants. The top 10 cuisines are displayed among all the restaurants.

Results
Restaurants that are less expensive are often more popular because they are affordable, while those with higher prices are liked for their perceived quality and exclusiveness. I was able to show that most of the restaurants are priced between 100-400. Making them a popular option for people due to their affordability. I equated the number of ratings a restaurant has to how popular the restaurant is, only 4% of restaurants have “number of ratings” above 1,000 which goes to show that not every restaurant can be popular. Looking at restaurants with more than 1000 number of ratings, restaurants with ratings above 4.0/5 have their average price between 100-300. The average price of restaurants goes up, the average rating the restaurants trends higher. Showing us that restaurants with higher prices are liked by people because of the quality and exclusiveness. Analyzing restaurants with more than 1000 number of ratings; we found that among these restaurants, we found that the top 3 most popular cuisines are juices, ice cream and Bhutanese food.