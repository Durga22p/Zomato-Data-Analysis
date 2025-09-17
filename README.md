# Zomato-Data-Analysis
_**Using Python**_

_**Understanding customer preferences and restaurant trends is important for making informed business decisions in food industry. Here, we will analyze Zomato’s restaurant dataset using Python to find meaningful insights. We aim to answer questions such as:**_

1. Do more restaurants provide online delivery compared to offline services?
2. Which types of restaurants are most favored by the general public?
3. What price range do couples prefer for dining out?

_**Implementation for Zomato Data Analysis using Python.**_

You can download the dataset from https://media.geeksforgeeks.org/wp-content/uploads/20250117023324808265/Zomato-data-.csv

Below steps are followed for its implementation.

**Step 1:** _Importing necessary Python libraries._

We will be using Pandas, Numpy, Matplotlib and Seaborn libraries.

**Step 2:** _Creating the data frame._

**Step 3:** _Data Cleaning and Preparation_

Before moving further we need to clean and process the data.

1. Convert the rate column to a float by removing denominator characters.

dataframe['rate']=dataframe['rate'].apply(handleRate): Applies the handleRate function to clean and convert each rating value in the 'rate' column.

2. Getting summary of the dataframe use df.info().

3. Checking for missing or null values to identify any data gaps.As a result, there is no NULL value in dataframe.

**Step 4:** Exploring Restaurant Types

1. Let's see the listed_in (type) column to identify popular restaurant categories.
   **_Conclusion:_** The majority of the restaurants fall into the dining category.

2. Votes by Restaurant Type
  Here we get the count of votes for each category.
 _**Conclusion:**_ Dining restaurants are preferred by a larger number of individuals.

**Step 5:** Identify the Most Voted Restaurant

Find the restaurant with the highest number of votes.

**Step 6:** Online Order Availability

Exploring the online_order column to see how many restaurants accept online orders.
**_Conclusion:_** This suggests that a majority of the restaurants do not accept online orders.

**Step 7:** Analyze Ratings

Checking the distribution of ratings from the rate column.
**_Conclusion:_** The majority of restaurants received ratings ranging from 3.5 to 4.

**Step 8:** Approximate Cost for Couples

Analyze the approx_cost(for two people) column to find the preferred price range.
_**Conclusion:**_ The majority of couples prefer restaurants with an approximate cost of 300 rupees.

**Step 9:** Ratings Comparison - Online vs Offline Orders

Compare ratings between restaurants that accept online orders and those that don't.

_**Conclusion:**_ Offline orders received lower ratings in comparison to online orders which obtained excellent ratings.

**Step 10:** Order Mode Preferences by Restaurant Type

Find the relationship between order mode (online_order) and restaurant type (listed_in(type)).

pivot_table = dataframe.pivot_table(index='listed_in(type)', columns='online_order', aggfunc='size', fill_value=0): Creates a pivot table counting restaurants by type and online order availability.

_**Conclusion:**_ With this we can say that dining restaurants primarily accept offline orders whereas cafes primarily receive online orders. This suggests that clients prefer to place orders in person at restaurants but prefer online ordering at cafes.
