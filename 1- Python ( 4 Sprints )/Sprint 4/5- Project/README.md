# 1- What ’re the methods that you used ?
      
   1. **Pandas**
        - read_csv()
        - head()
        - info()
        - describe()
        - isnull()
        - unique()
        - map()
        - value_counts()
        
   2. **seaborn**
        - heatmap()
        - countplot()
        - barplot()  

   3. **matplotlib.pyplot**
        - figure()
        - show()
        - pie()
        - legend() 
        - tight_layout()
        - title()
     
   4. **plotly**
        - create_distplot()
        - update_layout()
        - box()
        - update_layout() 
   
   5. train_test_split()

   6. SelectKBest
        - f_classif 
        - fit_transform

# 2- Explain each method ..

   - Read data using read_csv method
   - print some info about data using:
        - shape
        - info
        - describe
   - Rename data columns to be meaningful
   - Check null values
   - Convert data from encoding to categorical to be meaningful using:-
        - map and dictionary
   - plot heatmap of data to see features correlation using:-
        - sns.heatmap
   - countplot for target using:-
        - sns.countplot 
   - Count of male and female patients using:-
        - sns.countplot
   - plot age distribution using:-
        - plotly.figure_factory.create_distplot 
   - divide patients according to ages to:-
        - young_people from 29 to 40
        - mid_people from 40 to 55
        - old_people from 55 to higer
        - Then using pie chart, plot people ranges
   - plot Age and Target based on sex using:-
        - sns.barplot
   - plot for target and age based on sex using:-
        - plotly.express.box
   - Counts of Chest pain type among Heart Patients and Non-Heart Patients using:-
        - sns.countplot
   - Counts of Chest pain type among male and female patients using:-
        - sns.countplot
   - plot distribution of Resting Blood Pressure using:-
        - plotly.figure_factory.create_distplot
   - plot of Resting Blood Pressure with Target using:-
        - sns.barplot
   - plot Boxplot of Resting Blood Pressure with Target using:-
        - plotly.express.box
   - plot distribution of Serum Cholesterol using:-
        - plotly.figure_factory.create_distplot   
   - Plot of Resting Blood Pressure with Target using:-
        - sns.barplot
   - plot Boxplot of Resting Blood Pressure with Target using:-
        - plotly.express.box
   - Counts of Heart problem and No Heart problem Patients with fasting blood sugar above 120 mg/dl and lower than 120 mg/dl using:-
        - sns.countplot
   - Counts of Male and Female people with fasting blood sugar above 120 mg/dl and lower than 120 mg/dl using:-
        - sns.countplot
   - plot distribution of Maximum Heart Rate using:-
        - plotly.figure_factory.create_distplot
   - plot Maximum heart rate and target using:-
        - sns.barplot
   - plt Box plot on basis of sex using:-
        - plotly.express.box
   - split data to train and test using:-
        - train_test_split
   - select 8 best features using:-
        - SelectKBest 

# 3- What’s new for you ?

   - Plotty library

# 4- Resources ? 

   - https://stackoverflow.com/questions/20763012/creating-a-pandas-dataframe-from-a-numpy-array-how-do-i-specify-the-index-colum
   - https://seaborn.pydata.org/generated/seaborn.heatmap.html
   - https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.SelectKBest.html
   - https://pythonspot.com/matplotlib-pie-chart/
   - https://plotly.com/python/box-plots/
   - https://plotly.com/python/figure-factory-subplots/
