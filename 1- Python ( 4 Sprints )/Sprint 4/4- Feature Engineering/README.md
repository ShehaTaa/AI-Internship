# 1- What ’re the methods that you used ?

   1. **Baseline Model**
 
        - astype()
        - Series.dt 
          - dt.day
          - dt.hour
          - dt.minute
          - dt.second
        - LabelEncoder()
          - encoder.fit_transform() 

   2. **Categorical Encodings**

        - category_encoders
          - CountEncoder()
          - TargetEncoder()
          - CatBoostEncoder()
            
            - fit()
            - transform()
        - join()
        - add_suffix() 

   3. **Feature Generation**

        - itertools.combinations()
        - LabelEncoder()
        - fit_transform()
        - rolling()
        - series.diff()  
        - dt.total_seconds()
        - series.expanding()

   4. **Feature Selection**

        - SelectKBest()
        - fit_transform()
        - LogisticRegression()
        - SelectFromModel()  
        - transform()
        - var()

# 2- Explain each method ..

   1. **Baseline Model**
 
        - Create features for the coresponding day, hour, minute and second from 'click_time' column in dataset using:-
           - clicks['day'] = clicks['click_time'].dt.day.astype('uint8')
           - clicks['hour'] = clicks['click_time'].dt.hour.astype('uint8')
           - clicks['minute'] = clicks['click_time'].dt.minute.astype('uint8')
           - clicks['second'] = clicks['click_time'].dt.second.astype('uint8')

        - Encode each of the categorical features ['ip', 'app', 'device', 'os', 'channel'], useing scikit-learn's LabelEncoder
           - encoder = LabelEncoder()
           -  encoded_features = encoder.fit_transform()

        - Split dataset inro train, validate, and test data
          - 80% for train
          - 10% for valid
          - 10% for test
        - Then use LightGBM model to fit data

   2. **Categorical Encodings**

        - Select categorical features in a list to be encoded 
          - cat_features = ['ip', 'app', 'device', 'os', 'channel']

        1. Create the count encoder using:-
           - ce.CountEncoder(cols = cat_features)
        2. Fit CountEncoder object on data using:-
           - count_enc.fit(train[cat_features])
        3. Apply encoding to the train and validation sets as new columns and sake sure to add `_count` as a suffix to the new columns using:-
           - train_encoded = train.join(count_enc.transform(train[cat_features]).add_suffix("_count"))
           - valid_encoded = valid.join(count_enc.transform(valid[cat_features]).add_suffix("_count"))  
        4. fit the data to the model to train it using:-
           - _ = train_model(train_encoded, valid_encoded)
           - train model() --> is a fuction to build and train model based on lightgbm model.

        5. repeat the same steps [1 : 4] for TargetEncoder and CatBoostEncoder

   3. **Feature Generation**

        1. Add interaction features:-
           - add interaction features for each pair of categorical features (ip, app, device, os, channel)using: itertools.combinations.
           - Then encode the new features for training  using LabelEncoder()

        2. Number of events in the past six hours:-
           - Create the number of events from the same IP in the last six hours using :-
             - past_events = six_hour_series.rolling('6H').count() - 1
               - rolling('6H') --> Rolling sub-classed for the particular operation(past 6 hours)
               - -1 --> to exclude current event
   
        3. Features from future information:-
           - We shouldn't use information from the future.
           - Model's score will likely be higher when training and testing on historical data.

        4. Time since last event:-
           - Calculates the time since the last event in seconds from a Series of timestamps using:-
             - series.diff().dt.total_seconds()
               - Return total duration of each element expressed in seconds.

        5. Number of previous app downloads:-
           - Create a function returns a Series with the number of times an app has been downloaded ('is_attributed' == 1) before the current event using:-
             - series.expanding(min_periods = 2).sum() - series

   4. **Feature Selection**

        1. Which data to use for feature selection?
           - feature selection is performed on training set only
           - Then according to the results, we remove features from validation and test sets.

        2. Univariate Feature Selection:-
           - We define our selector using SelectKBest method as selector with f_classif, k = 40 as arguments 
           - Then using selector to fit on training data
           - Then return a dataframe of all data 
             - Selected data with their values
             - unselected data with 0 values
           - Finally, fit the selected data to the model

        3. Use L1 regularization for feature selection:-
           - Use LogisticRegression model to select features using:-
             - LogisticRegression(C = 0.1, penalty= 'l1', solver= 'liblinear', random_state= 7).fit(X,y)
           - then repeat the same steps of point 2 
         
# 3- What’s new for you ?

   - reviewing feature engineering
   - category_encoders library
   - Feature Generation
   - Feature Selection

# 4- Resources ? 

   - https://www.kaggle.com/matleonard/baseline-model
   - https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.dt.html
   - https://www.kaggle.com/matleonard/categorical-encodings
   - https://github.com/scikit-learn-contrib/category_encoders
   - https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.add_suffix.html
   - https://www.kaggle.com/matleonard/feature-generation
   - https://www.geeksforgeeks.org/python-itertools-combinations-function/#:~:text=Similarly%20itertools.,are%20emitted%20in%20lexicographical%20order.
   - https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.diff.html
   - https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.dt.total_seconds.html
   - https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.expanding.html
   - https://www.youtube.com/watch?v=XiFygkOVrA4
   - https://www.kaggle.com/matleonard/feature-selection
   - https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.SelectKBest.html
   - https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.f_classif.html#sklearn.feature_selection.f_classif
   - https://scikit-learn.org/stable/modules/feature_selection.html#univariate-feature-selection
   - https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html
   - https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.SelectFromModel.html




 
