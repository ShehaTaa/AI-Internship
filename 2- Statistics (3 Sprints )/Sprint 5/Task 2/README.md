# Summary of this videos

   - **Lesson 11 (Bayes Rule):-**
        - P(Pos, C)  = P(Pos|C) * P(C)
        - P(Neg, C)  = P(Neg|C) * P(C)
        - P(Pos, ~C) = P(Pos|~C) * P(~C)
        - P(Neg, ~C) = P(Neg|~C) * P(~C) 
        - P(C | Pos) = [P(pos | C) * P(C)] / P(Pos)
        - P(Pos | C)  --> Sensitivity
        - P(Neg | ~C) --> Specificity

   - **Lesson 12 (Programming Bayes Rule):-**
        - Programming Exercises about Bayes Rule 

   - **Lesson 13 (Probability Distributions):-**
        - In continuous distribution, every outcome has probability 0.
        - size of any interval P(a < x <= b) = |b - a| / 360
        - Density Function:-  
          - is an equation to mathematically represent a continuous distribution.
          - The area underneath a uniform continuous probability distribution is sum to 1.
        - Piece-Wise Continuous Probability Distributions

   - **Lesson 14 (Correlation vs Causation):-**
        - Correlation between data and it's impact on events.
        - if data have a confounding variable, best to omit it.
        - Reverse Causation, some variable referes to the same correlation. 
        - **Correlation:-**
            - Is a statistical measure (expressed as a number) that describes the size and direction of a relationship between two or more variables.  
        - **Causation:-**
            - Indicates that one event is the result of the occurrence of the other event.
        - The objective of correlation and causation analysis is to identify the extent to which one variable relates to another variable.
        - Causation explicitly applies to cases where action A causes outcome B.

   - **Lesson 15 (Problem Set 2: Probability):-**
        -  Exercises about basic probability and conditional probability. 

   - **Lesson 16 (Estimation):-**
        - The Maximum Likelihood Estimator **MLE**:-
          - Computed using empirical count 1/n * sum(Xi)
        - the Laplace Estimator:-
          - Computed using: 1 / n+k * (1 + sum(Xi))
            - K --> is fake data, number of outcomes 
            - n --> number of experiments
        - When their isn't much data, fake it.

   - **Lesson 17 (Averages):-**
        - Three M in Statistics is:-
          - Mean:-
            - Is the average computed by: 1/n * sum(Xi)  
          - Median:
            - Sort values, then peaks the value in the middle.  
          - Mode:-
            - Is the most frequent value.
            - Mode is consider the best representation of data in Bimodel and Multimodel.
   
   - **Lesson 18 (Variance):-**
        - Variance is:-
          - Measure how much the data is spread.
          - The average of the squared differences from the Mean.
          - Computed using:
            - 1/n * sum(Xi - mean)^2.  
            - (Sum(Xi^2) / N) - (sum(Xi)^2 / N^2)              
        - Standard Deviation (std):-
          - Measure of how spread out numbers are.
          - Is the square root of variance.
          - std = √variance
        - Standard Score to get how far point x from mean
          - computed by --> z = (X - mean) / std 

   - **Lesson 19 (Programming Estimators):-**
        - programming for:-
          - Mean
          - Median
          - Mode
          - Variance 
          - Standard Deviation

   - **Lesson 20 (Problem Set 3:Estimators):-**
        - Some Exercise on mean, mode, variance and std 
 
# What’s new for you ?

   - Reviewing some basics Statstics and probability.
   - Correlation vs Causation
   - Estimation Probability

   
# Additional Resources ? 
     
   - https://en.wikipedia.org/wiki/Piecewise 
   - https://discussions.udacity.com/t/correlation-vs-causation-assignment/186693
   - https://www.abs.gov.au/websitedbs/a3121120.nsf/home/statistical+language+-+correlation+and+causation#:~:text=A%20correlation%20between%20variables%2C%20however,relationship%20between%20the%20two%20events.
   - https://amplitude.com/blog/2017/01/19/causation-correlation
   - https://www.cs.cmu.edu/~tom/mlbook/Joint_MLE_MAP.pdf
   - https://www.cs.cornell.edu/courses/cs4780/2018fa/lectures/lecturenote04.html
   - https://medium.com/@mlengineer/generative-and-discriminative-models-af5637a66a3
   - https://en.wikipedia.org/wiki/Binomial_distribution
   - https://www.mathsisfun.com/data/standard-deviation.html




