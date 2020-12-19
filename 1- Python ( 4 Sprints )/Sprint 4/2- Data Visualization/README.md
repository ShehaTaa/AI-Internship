# 1- What ’re the methods that you used ?
 
   - **Line Charts:-**
        - sns.lineplot()  
        - plt.figure()
        - plt.title()
   
   - **Bar Charts and Heatmaps:-**
        - sns.barplot()
        - sns.heatmap()
        - plt.xlabel()
       
   - **Scatter Plots:-**
        - sns.scatterplot()
        - sns.regplot()
        - sns.lmplot()  
        - sns.swarmplot ()

   - **Distributions:-**
        - sns.distplot()
        - sns.kdeplot()

   - **Choosing Plot Types and Custom Styles:-**
        - sns.set_style

   - **Final Project:-**
        - sns.set()
        - sns.barplot()
        - plt.legend()
        - plt.xlabel()
        - plt.ylabel()
        - plt.title()
        - plt.show()
        - plt.figure()
        - plt.xticks()
        - sns.catplot()
        - sns.pointplot()
        - plt.pie()
        - plt.tight_layout()
        - sns.lmplot()
        - sns.kdeplot()
        - sns.heatmap()
        - sns.swarmplot

# 2- Explain each method ..

   - **Line Charts:-**
 
        - use lineplot method to show the trends and seasonality of the data using:-
          - sns.lineplot(data = museum_data)

        - use lineplot to show only one column -Avila Adobe- of the data using:-
          - sns.lineplot(data = museum_data['Avila Adobe'])
          - and put title for the chart

   - **Bar Charts and Heatmaps:-**

        - use barblot that shows the average score for racing games, for each platform using:-
          - sns.barplot(x = ign_data['Racing'], y = ign_data.index)
          - and put title for chart using plt.title()

        - Use the data to create a heatmap of average score by genre and platform using:-
          - sns.heatmap(data = ign_data , annot=True)
            - data --> our dataset
            - annot --> to make sure that every number will appear   

   - **Scatter Plots:-** 
         
        - Create a scatter plot that shows the relationship between 'sugarpercent' (on the horizontal x-axis) and 'winpercent' (on the vertical y-axis) using:- 
          - sns.scatterplot(x = candy_data['sugarpercent'], y = candy_data['winpercent'])

        - Create the same scatter plot, but now with a regression line using:- 
          - sns.regplot(x = candy_data['sugarpercent'], y = candy_data['winpercent'])

        -  create a scatter plot to show the relationship between 'pricepercent' (on the horizontal x-axis) and 'winpercent' (on the vertical y-axis) using:- 
          - sns.scatterplot(x = candy_data['pricepercent'], y = candy_data['winpercent'], hue = candy_data['chocolate'])

        - Create the same scatter plot, but now with two regression lines, corresponding to (1) chocolate candies and (2) candies without chocolate using:- 
          - sns.lmplot(x = 'pricepercent', y = 'winpercent',
           hue = 'chocolate', data = candy_data)
 
        - Create a categorical scatter plot to highlight the relationship between 'chocolate' and 'winpercent' using:-
          - sns.swarmplot(x = candy_data['chocolate'], y = candy_data['winpercent'])

   - **Distributions:-**
 
        - create two histograms that show the distribution in values for 'Area (mean)' for both benign and malignant tumors using:-
          - sns.distplot(a = cancer_b_data['Area (mean)'], kde = False)
          - sns.distplot(a = cancer_m_data['Area (mean)'], kde = False) 

        - create two KDE plots that show the distribution in values for 'Radius (worst)' for both benign and malignant tumors using:-
          - sns.kdeplot(data = cancer_b_data['Radius (worst)'], shade = True, label="Benign")
          - sns.kdeplot(data = cancer_m_data['Radius (worst)'], shade = True, label="Malignant")

   - **Choosing Plot Types and Custom Styles:-**
       
        - using sns.set_style, we can change style of our chart
          - "darkgrid"
          - "whitegrid"
          - "dark"
          - "white"
          - "ticks"         

# 3- What’s new for you ?

   - reviewing seaborn library

# 4- Resources ? 

   - https://seaborn.pydata.org/generated/seaborn.distplot.html
   - https://www.kaggle.com/alexisbcook/hello-seaborn
   - https://www.kaggle.com/alexisbcook/line-charts
   - https://www.kaggle.com/alexisbcook/bar-charts-and-heatmaps
   - https://www.kaggle.com/alexisbcook/scatter-plots
   - https://www.kaggle.com/alexisbcook/distributions
   - https://www.kaggle.com/alexisbcook/choosing-plot-types-and-custom-styles
   - https://seaborn.pydata.org/generated/seaborn.catplot.html
   - https://matplotlib.org/3.1.1/api/_as_gen/matplotlib.pyplot.pie.html
   - https://matplotlib.org/3.1.1/api/_as_gen/matplotlib.pyplot.legend.html
   - https://matplotlib.org/3.1.1/api/_as_gen/matplotlib.pyplot.tight_layout.html
   - https://seaborn.pydata.org/generated/seaborn.pairplot.html
   - https://seaborn.pydata.org/generated/seaborn.swarmplot.html
   - https://seaborn.pydata.org/generated/seaborn.heatmap.html
   - https://seaborn.pydata.org/generated/seaborn.kdeplot.html
   - https://seaborn.pydata.org/generated/seaborn.lmplot.html
