# 1- What ’re the methods that you used ?
  
   1. **Handling-missing-values**

        - isnull()
        - sum()
        - dropna()
        - fillna()
 
   2. **Scaling-and-normalization**  

        - minmax_scaling()
        - scipy.stats.boxcox()

   3. **Parsing-dates**

        - Series.str()
        - Series.str.len()
        - value_counts()
        - np.where()
        - Series.dt.day
        - sns.distplot()

   4. **Character-encodings**

        - decode()
        - encode()
        - open()
        - chardet.detect()
        - to_csv()
         
   5. **Inconsistent-data-entry**

        - str.strip()
        - unique()
        - sort()
        - fuzzywuzzy.process.extract()
 

# 2- Explain each method ..

   1. **handling-missing-values**

        - Get the percentage of the missing values in dataset by:-
          - calc count of all missing values
            - sf_permits.isnull().sum()
          - cal the count of all values, mul num rows with num cols
            - np.product(sf_permits.shape)
          - then div missing values and all values and mul by 100
            - (misiing_values_count / all_data) * 100

        - removed all of the rows of sf_permits with missing values, will remove all data in dataset 
          - sf_permits.dropna(axis = 0)

        - Get the number of the droped columns in dataset by:-
          - calc count of all droped columns with na values 
            - sf_permits.dropna(axis = 1)
          - cal the count of all columns
            - sf_permits.shape[1]
          - then sub droped columns from all columns
            -  dataset_cols - droped_cols

        - replacing all the NaN's in the sf_permits data with the one that comes directly after it and then replacing any remaining NaN's with 0 using:-
          - sf_permits.fillna(method = 'bfill', axis = 0).fillna(0)

   2. **Scaling-and-normalization**

        - Create a new DataFrame scaled_goal_data with values scaled between 0 and 1 using:-
          - minimax_scaling()

        - Normalize values of specific columns pledged using:-
          - pd.Series(stats.boxcox(positive_pledges)[0], 
            name = 'pledged', index = positive_pledges.index)
          - note that: Box-Cox only takes positive values  

   3. **Parsing-dates**

        - Check corrupted dtype of date and convert it manually by counting how many corrupted date using:-
          - date_lengths = earthquakes.Date.str.len()
            - Compute the length of each element in the Series
          - Then check specific condition to get the indices of corrupted date format 
            - indices = np.where([date_lengths == 24])[1]
          - Then change the format like that:-
            - earthquakes.loc[3378, 'Date'] = '02/23/1975'
          - Finally, change the format of column date from object to datetime format using:-
            - pd.to_datetime(earthquakes['Date'], format= '%m/%d/%Y')
              - %m --> match month
              - %d --> match day
              - %Y --> match year with four digits as 2020
              - %y --> match year with two digits as 20 

        - Create a Pandas Series day_of_month_earthquakes containing the day of the month from the "date_parsed" column using:-
          - earthquakes['date_parsed'].dt.day

        - Plot the days of the month from your earthquake dataset using:-  
          - sns.distplot(day_of_month_earthquakes, kde = False, bins = 31)

   4. **Character-encodings**

        - Create a variable new_entry that changes the encoding from "big5-tw" to "utf-8" using:-
          - before = sample_entry.decode("big5-tw")
          - new_entry = before.encode() 

        - open a file with different encode formate and use **chardet module** to detect it's encodeing type to can read it using:-
          - chardet.detect(myfile.read(100000))
          - then read the file with read_csv method with detected encoding type as argument

        - Then save the file as csv as the default encoding formate is UTF-8 


   5. **Inconsistent-data-entry** 
 
        - Extract unique values from specific columns using:-
          - unique() 
 
        - Convert every entry in the "Graduated from" column in the professors DataFrame to remove white spaces at the beginning and end of cells using:-
          - professors['Graduated from'].str.strip()

        - Extract unique values from specific columns using:-
          - unique() 
          - then sort them lphabetically using:-
            - sort()
          - Then correct the "Country" column in the dataframe so that 'usofa' appears instead as 'usa' using:-
            - fuzzywuzzy.process.extract("usa", countries, limit= 10,
                                           scorer= fuzzywuzzy.fuzz.token_sort_ratio)
              - limit= 10 --> retuen top 10 countries similar to usa
              - scorer= fuzzywuzzy.fuzz.token_sort_ratio --> sort simiral countries by it's score 
            - Then call the method
              - replace_matches_in_column(df = professors, column = 'Country', string_to_match = "usa", min_ratio = 70)


# 3- What’s new for you ?
 
   - stats.boxcox
   - Parsing dates
   - chardet module
   - fuzzywuzzy module

# 4- Resources ? 

   - https://www.kaggle.com/alexisbcook/handling-missing-values
   - https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.fillna.html
   - https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.boxcox.html
   - https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.html
   - https://www.kaggle.com/alexisbcook/parsing-dates
   - https://strftime.org/
   - https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.str.len.html
   - https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.str.html
   - https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.value_counts.html
   - https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.to_datetime.html
   - https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.dt.day.html
   - https://numpy.org/doc/stable/reference/generated/numpy.where.html
   - https://chardet.readthedocs.io/en/latest/usage.html
   - https://www.programiz.com/python-programming/methods/string/encode#:~:text=The%20string%20encode()%20method,sequence%20of%20Unicode%20code%20points.
   - https://www.tutorialspoint.com/python3/string_decode.htm
   - https://www.geeksforgeeks.org/fuzzywuzzy-python-library/
   - https://github.com/seatgeek/fuzzywuzzy
   - https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.str.strip.html
   













