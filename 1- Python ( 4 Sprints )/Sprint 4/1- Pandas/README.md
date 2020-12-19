# 1- What ’re the methods that you used ?

   - **Creating, Reading and Writing:-**<br />
        - DataFrame()
        - attribute: index, name
        - read_csv()
        - to_csv()

   - **Indexing, Selecting & Assigning:-**<br />
        - Columns, roews selection
        - iloc[]
        - isin()

   - **Summary Functions and Maps:-**<br />
        - median()
        - unique()
        - value_counts()
        - mean()
        - idxmax()
        - sum()
        - map()
        - apply()
        
   - **Grouping and Sorting:-**<br />
        - groupby()
        - max()
        - agg()
        - sort_values()
        - size()

   - **Data Types and Missing Values:-**<br />
        - dtype
        - astype()
        - isnull()
        - fillna()
        - value_counts()
        - sort_values()
        
   - **Renaming and Combining:-**<br />
        - rename()
        - rename_axis()
        - concat()
        - set_index()


# 2- Explain each method ..

  - **Creating, Reading and Writing:-**

        1. Create a dataFrame fruits using DataFrame

        2. Create a dataframe fruit_sales using DataFrame with index attribute

        3. Create a Series ingredients using Series with index and name attributes 
       
        4. Read a csv file using read_csv method

        5. Create a dataframe animals using DataFrame with index attribute

        6. convert animals dataframe created in step 5 to csv file using to_csv method.
             
 
  - **Indexing, Selecting & Assigning:-**

        1. Select the description column in reviews dataframe 

        2. Select the first value from the description column of reviews using:-
           - reviews.description.iloc[0] method.
      
        3. Select the first row of data (the first record) from reviews using:-
           - reviews.iloc[0]

        4. Select the first 10 values from the description column in reviews using:-
           - reviews.description[0:10]

        5. Select the records with index labels 1, 2, 3, 5, and 8 using:-      
           - reviews.iloc[[1, 2, 3, 5, 8]] with the use of list inside iloc.

        6. Create a df containing the country, province, region_1, and region_2 columns of the records with the index labels 0, 1, 10, and 100 using:-
           - reviews.loc[[0,1,10,100],['country', 'province', 'region_1', 'region_2']
             - [0,1,10,100] --> To specify the index.
             - ['country', 'province', 'region_1', 'region_2'] --> To specify the columns.

        7.Create a df containing the country and variety columns of the first 100 records using:-
           - reviews.loc[:99, ['country', 'variety']]
             - :99 --> To specify the first 100 records
             - ['country', 'variety'] --> To specify the columns.

        8. Create a DataFrame italian_wines containing reviews of wines made in Italy using:-
           - reviews[reviews.country == 'Italy'] 
             - reviews.country == 'Italy' --> condition to select reviews of wines made in Italy 

        9. Create a DataFrame top_oceania_wines containing all reviews with at least 95 points (out of 100) for wines from Australia or New Zealand using:- 
           - reviews[(reviews.points >= 95) & reviews.country.isin(['Australia', 'New Zealand'])]
             - (reviews.points >= 95) --> select all reviews with at least 95 points
             - reviews.country.isin(['Australia', 'New Zealand']) --> select reviews from Australia or New Zealand
             - & --> to specify the the two condition must be true
 

  - **Summary Functions and Maps:-**  

        1. Get median of the points column in the reviews using:-
           - median()
 
        2. Get unique countries in the dataset without duplicates using:-
           - unique()
  
        3. Specify how often each country appear in the dataset using:-
           - value_counts()
  
        4. Create a new price where each price value is subtracted from the mean price value using:-
           - reviews.price - reviews.price.mean()

        5. Create a variable bargain_wine with the title of the wine with the highest points-to-price ratio in the dataset using:-
           - reviews.iloc[(reviews['points'] / reviews['price']).idxmax()].title

        6. Create a Series descriptor_counts counting how many times each of these two words "tropical" or "fruity" appears in the description column in the dataset usnig:-
           - map(lambda x: 'tropical' in x) and map(lambda x: 'fruity' in x) to specify how many times each of these two words appears in the description column 
           - then using sum() to sum the number of occurance of each of the two words.

        7. - Create a function to return specific value under occurance of specific conditions.
           - using apply method to apply the created function on our dataframe.

       
  - **Grouping and Sorting:-**
 
        1. Create a Series whose index is the taster_twitter_handle category from the dataset, and whose values count how many reviews each person wrote using:-
           - groupby('taster_twitter_handle').taster_twitter_handle.count()

        2. Create a Series whose index is wine prices and whose values is the maximum number of points a wine costing using:-
           - groupby('price').points.max()
       
        3. Create a DataFrame whose index is the variety category from the dataset and whose values are the min and max values using:-
           - reviews.groupby('variety').price.agg(['min','max'])

        4. Create a variable sorted_varieties containing a copy of the dataframe from the previous question where varieties are sorted in descending order based on minimum price, then on maximum price using:- 
           - price_extremes.sort_values(by = ['min','max'], ascending = False)

        5. Create a Series whose index is reviewers and whose values is the average review score given out by that reviewer using:-
           - reviews.groupby('taster_name').points.mean()

        6. Create a Series whose index is a MultiIndexof {country, variety} pairs using:-
           - reviews.groupby(['country', 'variety']).size().sort_values(ascending = False) 
             - size() --> to get the length of the groubed columns
             - sort_values(ascending = False) --> to sort the values in deccending order

       
  - **Data Types and Missing Values:-**

        1. Specify the data type of the points column using:-
           - dtype property

        2. Convert the data type of the points column to strings using:-
           - astype('str')
       
        3. Specify how many reviews in the dataset are missing a price using:- 
           - isnull().sum()
       
        4.- Create a Series counting the number of times each value occurs in the region_1 field.
          - This field is often missing data, so replace missing values with Unknown.
          - Sort in descending order.
          - using:- 
           - reviews.region_1.fillna('Unknown').value_counts().sort_values(ascending=False)


  - **Renaming and Combining:-**

        1. Rename columns region_1 and region_2 to region and local using:-
          - reviews.rename(columns = {'region_1':'region', 'region_2':'locale'})

        2. set wines column to be the index of dataset using:-
          - reviews.rename_axis("wines", axis = 'rows')

        3. merging two dataframe using concat method

        4. merging two dataframe using join method after set index of the two dataframe frist using:-
          - powerlifting_meets.set_index("MeetID")
           .join(powerlifting_competitors.set_index("MeetID"))



# 3- What’s new for you ?
 
   - Reviewing pandas library


# 4- Resources ? 

   - https://www.kaggle.com/residentmario/creating-reading-and-writing
   - https://www.kaggle.com/residentmario/indexing-selecting-assigning
   - https://www.kaggle.com/residentmario/summary-functions-and-maps
   - https://www.kaggle.com/residentmario/grouping-and-sorting
   - https://www.kaggle.com/residentmario/data-types-and-missing-values
   - https://www.kaggle.com/residentmario/renaming-and-combining

    
