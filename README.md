
![alt tag](https://github.com/colorxyz/AirBnb_Analysis/blob/main/extra/airsmall.png)
# BOSTON and SEATLE AIRBNB OPEN DATA ANALYSIS

In this Project, I am going to explore the Airbnb data of Boston and Seatle which includes 3 files:

* listings.csv 
* calendar.csv
* reviews.csv

**Boston/(Seatle/)listings csv** consists of details of all the listings in Boston & Seatle including their price, accomodates, ratings, number of reviews, summary, name, owner name, description, host Id and many other columns decribing details of listings.

**Boston/(Seatle/)calendar.csv** consists of details of listings and its availability and its price.

**Boston/(Seatle/)reviews.csv** consits of reveiws for each listing in Boston

This includes 3 analysis on Boston and Seatle Airbnb open dataset with the help of which I tried to answer questions like seasonal pattern of airbnb housing price? and many more


## ANALYSIS - 1 
## WHAT CAUSES DIFFERENCE IN PRICES OF LISTINGS?

![alt tag](https://github.com/colorxyz/AirBnb_Analysis/blob/main/Output%20Graphs/Distribution_of_Prices_of_Airbnbs1.png)

![alt tag](https://github.com/colorxyz/AirBnb_Analysis/blob/main/Output%20Graphs/Distribution_of_Prices_of_Airbnbs2.png)

It can be observed that we have quite skewed distributions, where the values of the prices vary up to $1300 in Boston and $1000 in Seatle.



I categorized different listings based upon their room type which gave the following results:

**Boston**

Room Type  | Number Of Listings
------| --------  
Entire home/apt|   1393    
Private room  |   1061       
Shared room  |   52     

![alt tag](https://github.com/colorxyz/AirBnb_Analysis/blob/main/Output%20Graphs/Room_Type_Distribution1.png)

**Seatle**

Room Type  | Number Of Listings
------| --------  
Entire home/apt|   1805    
Private room  |   947       
Shared room  |   91    

![alt tag](https://github.com/colorxyz/AirBnb_Analysis/blob/main/Output%20Graphs/Room_Type_Distribution2.png)

    It can be concluded that people are more inclined towards listing their entire property than that of private rooms or shared rooms.
    We can also find that Seatle has more rate to have "Entire home/apt" compare to Boston.
    It seem to me that house price can impact to this distribution.

I categorized different listings based upon their property type which gave the following results:

**Boston**

![alt tag](https://github.com/colorxyz/AirBnb_Analysis/blob/main/Output%20Graphs/Property_Type1.png)

**Seatle**

![alt tag](https://github.com/colorxyz/AirBnb_Analysis/blob/main/Output%20Graphs/Property_Type2.png)


### 1st Data point:
It can be concluded that people are more inclined towards listing their entire property than that of private rooms or shared rooms. It can also be seen that property type also plays an important factor. Not surprisingly, Apartment and houses take up an overwhelming majority of all listings, although we do see few instances unfamiliar residencies here and there.

We can also find that Seatle has more "House" property_type compare to Boston and they have different property type.



While plotting the same on a heat map:

![alt tag](https://github.com/colorxyz/AirBnb_Analysis/blob/main/Output%20Graphs/heat1.png)

![alt tag](https://github.com/colorxyz/AirBnb_Analysis/blob/main/Output%20Graphs/heat2.png)

![alt tag](https://github.com/colorxyz/AirBnb_Analysis/blob/main/Output%20Graphs/Property_Type.png)

### 2nd Data point:
This chart allows us to see all the listings' prices broken down by property type and room type. This gives us a much better understanding of the price breakdown based on property and room types.
It can be analyzed that for almost all property type,prices for Entire home/apartment is the maximum.This tells us that Property type and room type plays a very important role in deciding price of a listing.
We can find that Townhouse is maximum in Boston while Boat is maximum in Seatle.
I think that regional characteristics can affect to this.

Lets see how the number of bedrooms available affects the price of a listing

**Boston**

![alt tag](https://github.com/colorxyz/AirBnb_Analysis/blob/main/Output%20Graphs/heat3.png)

**Seatle**

![alt tag](https://github.com/colorxyz/AirBnb_Analysis/blob/main/Output%20Graphs/heat4.png)

### 3rd Data Point:
It can be analyzed that with the increase in the number of bedrooms price of listing increases.Although, it depends upon the neighbourhood as well.

So the analysis gives us data points that the prices of listings on Airbnb depends upon the room type, property type, number of bedrooms and neighbourhood.
It can be seen that the property with type as Apartment and the listing as with type as entire house with maximum number of bedooms has highest price.
Although it depends upon neighbourhood as well.
Seatle has many neighbourhood data and it has more impact to price compare to Boston.



## Conclusion: 
It can be concluded that prices of listings depends upon following factors:

1. The type of room chosen by the traveller and mostly booking an Entire property costs maximum followed by private room and shared apartment.
2. The type of property chosen by the traveller and it can be analyzed that Townhouse and houses are the properties with maximum prices and apartments, houses take up an overwhelming majority of all listings.
3. Price of a listing also depends upon the number of bedrooms the property have and the same also depends upon the neighborhood of the property



## ANALYSIS - 2 
## SEASONAL PATTERN OF PRICES

It can be seen that the Boston data is available from September 2016 to September 2017 and when average prices are analyzed maximum rates for the listings were in the month of september.
Visualizing the same for a better understanding.

**Boston**

![alt tag](https://github.com/colorxyz/AirBnb_Analysis/blob/main/Output%20Graphs/trend1.png)

**Seatle**

![alt tag](https://github.com/colorxyz/AirBnb_Analysis/blob/main/Output%20Graphs/trend2.png)

### 1st Data Point :
It can be clearly seen that the maximum average price for listings were in the month of september and October 2016 for Boston and the reason is because of good weather and Massachussetts' best time to observe fall colors.Fall Colors in Massachusetts attracts a lot of visitors which makes September and October peak months for Airbnb hosts. 

On the other hand, the maximum average price for listings were in the month of July and Aug 2016 for Seatle. It seems to me that Seatle is busy during Summer season.


To analyze the data further, I have extracted name of the day from given date and checked weather it was a holiday and what is the reason for that holiday using datetime, calendar and holidays modules of python.


Added 3 new columns Day_Name, Holiday and us_holiday_name which counsits of name of the day, boolean value for "is it a holiday?" and reason for the holiday respectively.

Trying to find a trend of avergae prices for a week

**Boston**

day_Name	|Average_Price|	day_num
-----------|-------------|---------
Monday	|195.809561	|1
Tuesday|	195.173842|	2
Wednesday|	195.418228	|3
Thursday|	198.073112	|4
Friday|	203.121167	|5
Saturday|	203.408387|	6
Sunday	|198.219764|	7

![alt tag](https://github.com/colorxyz/AirBnb_Analysis/blob/main/Output%20Graphs/Average_Price1.png)

**Seatle**

day_Name	|Average_Price|	day_num
-----------|-------------|---------
Monday	|135.676414	|1
Tuesday|	135.408764|	2
Wednesday|	135.447880	|3
Thursday|	136.476032	|4
Friday|	143.036294	|5
Saturday|	143.202136|	6
Sunday	|136.459941|	7

![alt tag](https://github.com/colorxyz/AirBnb_Analysis/blob/main/Output%20Graphs/Average_Price2.png)

It can be seen that the average price of listings increases on weekends and are usual on weekdays.


### 2nd Data Point
It can be seen that the prices are fairly high for the weekends than that of weekdays. 

Analyzing all the holidays

**Boston**

![alt tag](https://github.com/colorxyz/AirBnb_Analysis/blob/main/Output%20Graphs/holiday_Boston.png)

**Seatle**

![alt tag](https://github.com/colorxyz/AirBnb_Analysis/blob/main/Output%20Graphs/holiday_Seatle.png)

It can be seen that the maximum number of listings is for thanksgiving for Boston and New Year's day for Setale which can be reasoned as its a very popular holiday.
Lets dig in further to find which holiday has the maximum average price.

**Boston**

![alt tag](https://github.com/colorxyz/AirBnb_Analysis/blob/main/Output%20Graphs/holiday_Boston_Price.png)

![alt tag](https://github.com/colorxyz/AirBnb_Analysis/blob/main/Output%20Graphs/holiday_Boston_Price2.png)

**Seatle**

![alt tag](https://github.com/colorxyz/AirBnb_Analysis/blob/main/Output%20Graphs/holiday_Seatle_Price.png)

![alt tag](https://github.com/colorxyz/AirBnb_Analysis/blob/main/Output%20Graphs/holiday_Seatle_Price2.png)



## Conclusion:

After adding up all the analysis done so far for observing seasonal changes in prices,it can be concluded that:

1. If a traveller is visiting Boston on a low budget then he should avoid visiting during September and October as these are the times when average price of listings are fairly high as compared to the other months.
 If a traveller is visiting Seatle on a low budget then he should avoid visiting during July and August as these are the times when average price of listings are fairly high as compared to the other months.

2. If the taveller is on low budget then he should avoid visiting Boston and Seatle on Weekends as prices of listings on weekend are higher than that of weekdays.

3. Prices of listings also depends upon US holidays and long weekends. Prices on long weekends and US holidays are higher than compared to other days.
  So for a low budget travel, a traveller should avoid travelling on a long weekend,Specially the long weekend of October (i.e columbus day) for Boston and New Year's day for Seatle.


## ANALYSIS - 3 
## SENTIMENT ANALYSIS OF REVIEWS & ITS RELATION WITH PRICE

There are so many factors which contributes towards the price of a listing on AirBnB. While, we already have few conclusions for relationship between various factors and their dependency on prices of a listing, lets analyze if price of a listing dependent upon number of reviews and if yes, how does it varies?


To retrieve the 'sentiment' of comments - 'positive','negative' or 'neutral' I am using built-in analyzer in the NLTK Python library to assign polarity scoore to each comment. I have assigned Ploarity score to every comment which includes detail like Positivity, negativity 
neutral and compound.

listing_id	|id|reviewer_id|comments	|polarity_value	|neg	|pos	|neu	|compound
------------|-----|---------------|--------------|------------------|------|--------|-------|-------------
1178162	|4724140|	4298113	|My stay at islam's place was really cool! Good...	|{'neg': 0.0, 'neu': 0.648, 'pos': 0.352, 'comp...|	0.0	|0.352|	0.648	|0.9626
1178162	|4869189|6452964|Great location for both airport and city - gre...	|{'neg': 0.0, 'neu': 0.639, 'pos': 0.361, 'comp...	|0.0|	0.361	|0.639|	0.9061


Our data presented in the dataframe consists of comments in various language while we are concerned only with comments in English language. In the next section I am removing all those rows which consists of comments in different language than that of English using langdetect library.


listing_id	|id|reviewer_id|comments	|polarity_value	|neg	|pos	|neu	|compound |language
------------|-----|---------------|--------------|------------------|------|--------|-------|-------------|----
1178162	|4724140|	4298113	|My stay at islam's place was really cool! Good...	|{'neg': 0.0, 'neu': 0.648, 'pos': 0.352, 'comp...|	0.0	|0.352|	0.648	|0.9626|en

I created graphs to visualize the positive, negative anf neutral score by dividing thernage from 0.0 to 1.0 and counting the reviews between this range.

count_of_Comments	|RANGE	|Sentiment
-------------------|---------|---------
2143	|0.0|	positive
11940	|0.1	|positive
18092	|0.0	|negative
1447	|0.1	|negative
9|	0.0	|neutrl
204	|0.1	|neutrl

Plotted a factorgraph to undersatnd and compare the sentiments of comments travellers mentioned on the listings.

![alt tag](https://github.com/colorxyz/AirBnb_Analysis/blob/main/Output%20Graphs/sentiment.png)

### 1st Data Point:

It can be seen that Almost none of the texts are classified as having significant amounts of negativity. In fact, a significant amount of them are given exactly 0.0 negativity.It can be clearly seen that most of the comments are neutral.However, a signifigant amount of comments are positive.

We can loosely interpret number of reviews as times people have stayed in the said listing. Of course, this depends on when the listing appeared, how long it appeared for, and various other factors. But it could serve to be useful information to see correlation between price and number of reviews.Lets check if there is any relationship between number of reviews and price of listing.

![alt tag](https://github.com/colorxyz/AirBnb_Analysis/blob/main/Output%20Graphs/review.png)

### 2nd Data Point:

The graph shows that listings with prices that range around 100 - 400 get the most reviews, probably because they are in the most reasonable price range. 
The number quickly declines as the price goes up.
This indicates that more people book listings that are around $100 - 400 in prices for Boston while listings for Seatle are around $50~100.
This shows that it is not necessary for an expensive listing to have large number of reviews.
Heneforth there is no exact relation between Prices and Number of Reviews for a listing.

## Conlcusions:

1. It can be clearly seen that most of the comments are neutral and a signifigant amount of comments are positive and almost none of the texts are classified as having significant amounts of negativity.
2. Its clearly visible that listings with prices that range around 100 - 400 get the most reviews, probably because they are in the most reasonable price range. The number quickly declines as the price goes up.


## Addtional Instructions to Run the code

install mentioned libraries

* pip install holidays

