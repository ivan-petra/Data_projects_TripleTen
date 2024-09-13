TripleTen Sprint 6 Project - Power BI Project
This is the 6th project I worked on in the TripleTen BI Analyst program. 

Shopify App Analysis (https://www.loom.com/share/1b4ddb90df7f41b99f1dfaaafdbde582?sid=7fa27670-ba7f-40bd-914a-137c0f36b052)
The project task was to review the landscape of apps on the Shopify platform and figure out what key factors play into the success of a Shopify app

The Data

Dataset from the 'app' table - Details of the apps on Shopify apps marketplace
'id' : unique ID for the app
'developer' : name of the developer of the app
'rating	' : the rating of the app
'reviews_count' : the number of ratings the app received
'description' :	description of the app
'tagline' : tags pertaining to the app
'pricing_hint' : the cost of the app	
'lastmod' : the latest update to the app

Dataset from the 'review' table - Each review (row) contains information on user opinion about the related app (rating and comment). Also, it contains the response from the developer if present.
'app_id' : unique ID of the review
'author' : who wrote the review
'rating' : the rating the author left for the app
'posted_at' : when the review was posted
'body' : the review the author wrote
'helpful_count' : the number of people that found the review helpful
'developer_reply' : the response of the developer to the review
'developer_reply_posted_at' : when the developer responded to the review


The Process
Part 1: App Landscape
Using the Apps table. I made a new sheet in Power BI called App Landscape. Then I made a KPI Card (a visual with a single number) that counts the unique number of apps. Add it to your App Landscape sheet. Next I created a Line Chart getting the sum of the review count on the Y-axis, and the lastmod date on the X-Axis; making sure that the lastmod date is not in the “date hierarchy” format. Finally, I made a Scatterplot with the reviews_count on the X axis and the average rating on the Y axis. 

Part 2: Reviews
Made a new sheet in the .pibx file  named Reviews.

Created a new Column in the Reviews table named helpful_reviews using a DAX expression, which multiplies the rating by 1+helpful_count to weigh the reviews by how helpful they’ve been found. The made a Card with the average value of the new helpful_reviews column.
Then I created a new Column in the Reviews table named developer_answered using a DAX expression, which is 1 (or TRUE) if the developer_reply column is not blank and 0 (or FALSE) if the column row is blank. To finish off the section, I made a scatterplot comparing the average rating on the Y-Axis by the value of the developer_answered column on the X-Axis.

Part 3: App Reviews
Made a new sheet in the .pibx file. In the data model, I created a new relationship between the Reviews table and the Apps table. Use the app_id column from the Reviews table, the id column from the Apps table and I made the relationship many-to-one built as many (Reviews table) to one (Apps table). Using this new table, I made a bar chart with the developer on the X-Axis, and the sum of rating on the Y-Axis. Then I made a new bar chart with developer on the X-Axis against the helpful_review average on the Y-Axis.

To figure out which developers are the most responsive, I made a bar chart with the developer from the apps table and the developer_answered column then I  added a Filter for this visual only which selects only the rows where reviews_count is greater than 500.

Results
Part 1: App Landscape
There are 7341 unique apps on the Shopify App platform. Looking at the scatterplot, we can see that the apps on the Shopify platform have great reviews with majority of the ratings being above 4.0/5

Part 2: Reviews
the average value of the new helpful_reviews column is 5.48

Part 3: App Reviews
The most responsive developers are as follows: FireApps, DSers, PageFly, Privy, and ReConvert

