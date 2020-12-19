# 1- What ’re the methods that you used ?

   * **read_csv**
      - shape
      - dtypes
      
   * **describe**
      - include as argument
   * rename 
   * isin
   * **mean**
      - axis =0 or 1 as argument
   * groupby
   * value_counts
   * isnull()


# 2- Explain each method ..

   1. Read **csv file :-**
       - print first 5 row
       - print **shape** of file
       - print **type** of columns
   
   2. Print **carat** column
       - concatenate cut and color columns in new Quality-color column
   
   3. Use **info and describe** to describe the data and use float64 as argument to describe
      columns with floaet64 type only
        
   4. Use pandas condition to print values which match this conditions
   
   5. Rename columns using pandas **rename** method with columns as argument
   
   6. Use **isin** method to print only values which matche values in isin method
   
   7. - Use for loop to print columns name
      - Mean with **axis = 0** to calc mean of columns
      - Mean with **axis = 1** to calc mean of rows
      <br />
        
   8. - Use **mean** method to calc mean of price
      - Use **gropby** to calc mean of price according to cut values
      - Use **groupby and agg method** to print max, min, and count of cut values.
        - Dataframe.aggregate() function is used to apply some aggregation across one or more column.<br />
        - Aggregate using callable, string, dict, or list of string/callables.<br />
        - Most frequently used aggregations are<br />
          - sum: Return the sum of the values for the requested axis<br />
          - min: Return the minimum of the values for the requested axis<br />
          - max: Return the maximum of the values for the requested axis<br />
          - count: Return the count of the values for the requested axis<br />
        - Syntax: DataFrame.aggregate(func, axis=0)<br />
          - func : callable, string, dictionary, or list of string/callables.<br />
          - axis : (default 0) {0 or ‘index’, 1 or ‘columns’}<br />
      - Use **value_counts** to count the occurance of each value of cut
    
   9. Use **isnull** method to check if there is null values in dataframe or not 

# 3- What’s new for you ?

   - DataFrame aggregate


# 4- Resources ? 

   - https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.agg.html
   - https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.rename.html
   - https://www.geeksforgeeks.org/python-pandas-dataframe-aggregate/
   - https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_csv.html
