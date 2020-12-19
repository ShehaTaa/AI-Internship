# Summary of this videos

   - **Lesson 1 - Classification Problems**
        - Is a type of supervised learning. 
        - It specifies the class to which data elements belong to and is best used when the output has finite and discrete values.
        - It predicts a class for an input variable as well.
        - There are 2 types of Classification: 
          1. Binomial (Binary)
          2. Multi-Class (Non-Binary)
        - Target Variable (Dependent)
          - The field we are trying to predict
        - Predictor Variable (Independent)
          - Used to predict the target variable  
        - Dupliace Variable
          - Variable that does the exact same thing as another variable 
          - We remove those variable
        - **Correlation**:-
            - Measure of association between two variables
              - Correlation between -1 and 1  
              - **1** Positive Correlation 
              - **0** No Correlation
              - **-1** Negative Correlation  
          - **Correlation Methods**: -
              - Pearson
              - Spearman
              - Hoeffding   
        - Prepare data for modeling by cleaning it through
          1. remove dupliace variable
          2. remove null values     
              
   - **Lesson 2 - Binary Classification Problems**   
        1. **Logistic Regression**
             - Is one of the most basic forms of regression modeling.
             - It’s part of a family of “generalized linear models” or GLM for short.  
             - Is a classification algorithm.
             - It is used to predict a binary outcome (1 / 0, Yes / No, True / False) given a set of independent variables.
             - **Prepare Data for Logistic Regression**
                 1. Binary Output Variable
                    - logistic regression is intended for binary (two-class) classification problems
                 2. Remove Noise
                    - No error in the output variable (y)
                    - Removing outliers and possibly misclassified instances from your training data.  
                 3. Gaussian Distribution
                    - Logistic regression is a linear algorithm (with a non-linear transform on output).
                    - It does assume a linear relationship between the input variables with the output.  
                 4. Remove Correlated Inputs
                    - The model can overfit if you have multiple highly-correlated inputs.    
                 5. Fail to Converge
                    - It is possible for the expected likelihood estimation process that learns the coefficients to fail to converge.
                    - This can happen if there are many highly correlated inputs in your data or the data is very sparse   
             - To represent binary/categorical outcome, we use dummy variables.
               - **Dummy variables**
                   - variables with only two values, zero and one
             - **logistic regression equation**:
                  y = e^(β0 + β1*x) / (1 + e^(β0 + β1*x))      
             - **Stepwise Regression**
                 - is a process where variable are added and/or removed untill the best combination of variable is identified   
        
        2. **Decision Tree**
             - Is the most powerful and popular tool for classification and prediction.
             - Is one of the most widely used and practical methods for supervised learning.
             - are a non-parametric supervised learning method used for both classification and regression tasks.
             - Is a flowchart like tree structure, where
               - each internal node denotes a test on an attribute
               - each branch represents an outcome of the test
               - each leaf node (terminal node) holds a class label.      
             - **Steps for Making decision tree** 
                 1. Get list of rows (dataset) which are taken into consideration for making decision tree (recursively at each nodes).
                 2. Calculate uncertanity of our dataset or Gini impurity or how much our data is mixed up etc.
                 3. Generate list of all question which needs to be asked at that node.
                 4. Partition rows into True rows and False rows based on each question asked.
                 5. Calculate information gain based on gini impurity and partition of data from previous step.
                 6. Update highest information gain based on each question asked.
                 7. Update best question based on information gain (higher information gain).
                 8. Divide the node on best question. Repeat again from step 1 again until we get pure node (leaf nodes). 
             - **Information Gain**
                 - Is used to decide which feature to split on at each step in building the tree.             
             - **Gini Impurity**
                 - Is a measurement of the likelihood of an incorrect classification of a new instance of a random variable
                 - If that new instance were randomly classified according to the distribution of class labels from the data set.
             - **Confusion Matrix**
                 - A matrix (or table) that lists out all of the possible prediction results when we validate our model against our validation set. 
                 - This confusion matrix is one of the best methods to review the accuracy and precision of your model as well as to understand any model bias in classifying your data points.    
         
        - **ROC curve**
            - is a commonly used way to visualize the performance of a binary classifier, meaning a classifier with two possible output classes.

   - **Lesson 3 - Non-Binary Classification Problems** 
        1. **Decision Tree**
             - are prone to an error called over fitting, where          - the model fits the sample data too well,
               - and as a result, does not predict future results as well as it should.
             
        2. **Forest Model**
             - Is a supervised learning algorithm.
             - The "forest" it builds, is an ensemble of decision trees, usually trained with the “bagging” method.
             - The general idea of the bagging method is that a combination of learning models increases the overall result.
             - Each individual tree created still has overfitting issues, but when you look at the results as a whole, the overfitting gets averaged out by all of the other trees.
             
             - **Out of the Bag Error Rate**
                 - Explains how well the model performed with the cross-validation set in the estimation data. 
                 - This gives a good understanding of how solid the model performs with just the estimation data.
             - **Confusion Matrix** 
                 - Shows again how well the model performed on the original, estimation data.
                 - Compared to the "Out Of The Bag Error Rate", the confusion matrix does a better job at representing where errors occurred in classifying the data.   
        
        3. **Boosted Models**    
             -  Might give us a better estimate than decision trees, but they're computationally intensive.   
             - **How the Boosted model avoids overfitting**
                 1. Instead of creating a bunch of random trees, the boosted model makes one tree.
                 2. Algorithm performs an analysis on the errors of the tree to identify the biggest source of error.
                 3. Changes the tree to reduce that error.
                 4. Does the analysis again to find the next biggest error.
                 5. Makes a change to reduce it.
                 6. Does this over and over until it can’t make the tree any better and we have our finished Boosted Model.      
             - **Boosted Models types**
                 - AdaBoost
                 - Gradient boosting
                   - generalization of AdaBoosting    
                 - XGBoost 
                 - LightBoost      
    
# What’s new for you ?

   - Boosted Models

# Resources ? 

   - https://www.simplilearn.com/classification-machine-learning-tutorial#:~:text=Classification%20is%20a%20type%20of,an%20input%20variable%20as%20well.
   - https://en.wikipedia.org/wiki/Pearson_correlation_coefficient
   - https://en.wikipedia.org/wiki/Spearman's_rank_correlation_coefficient
   - https://en.wikipedia.org/wiki/Hoeffding's_independence_test
   - https://help.alteryx.com/10.1/index.htm#cshid=Oversample_Field.htm
   - https://en.wikipedia.org/wiki/Logistic_regression#:~:text=Logistic%20regression%20is%20a%20statistical,a%20form%20of%20binary%20regression).
   - https://www.analyticsvidhya.com/blog/2015/11/beginners-guide-on-logistic-regression-in-r/#:~:text=For%20any%20value%20of%20slope,equation%20will%20never%20be%20negative.&text=log(p%2F1%2Dp,association%20in%20a%20linear%20way.&text=This%20is%20the%20equation%20used%20in%20Logistic%20Regression.
   - https://dss.princeton.edu/online_help/analysis/dummy_variables.htm
   - https://machinelearningmastery.com/logistic-regression-for-machine-learning/
   - https://www.geeksforgeeks.org/decision-tree/
   - https://towardsdatascience.com/decision-tree-in-machine-learning-e380942a4c96
   - https://www.dataschool.io/roc-curves-and-auc-explained/
   - https://www.quora.com/What-is-Precision-Recall-PR-curve
   - http://www2.cs.uregina.ca/~dbd/cs831/notes/lift_chart/lift_chart.html
   - https://www.quora.com/What-is-an-intuitive-explanation-of-over-fitting-particularly-with-a-small-sample-set-What-are-you-essentially-doing-by-over-fitting-How-does-the-over-promise-of-a-high-R%C2%B2-low-standard-error-occur
   - https://builtin.com/data-science/random-forest-algorithm
   - https://stats.stackexchange.com/questions/26088/explaining-to-laypeople-why-bootstrapping-works
   - https://towardsdatascience.com/boosting-algorithms-explained-d38f56ef3f30
   - https://machinelearningmastery.com/gradient-boosting-machine-ensemble-in-python/
