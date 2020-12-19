# Summary of this videos

   - **Lesson 21 (Outlires):-**
        - **Outlires** should excluded from calculations. 
        - **Quartiles** are the values that divide a list of numbers into quarters:
            - Put the list of numbers **in order.**
            - Then cut the list into **four equal parts.** 
            - The Quartiles are at the "cuts."
            - Interquartile Range is from Q1 to Q3:-
              - To calculate it just subtract Quartile 1 from Quartile 3 
        - **Percentiles** the value below which a percentage of data falls.
            - Quartile 1 (Q1) can be called the **25th percentile**
            - Quartile 2 (Q2) can be called the **50th percentile**
            - Quartile 3 (Q3) can be called the **75th percentile**

   - **Lesson 22 (Binomial Distribution):-**
        - We have a coin with p(heads) = p
        - Flip the coin n times 
        - to get p(#heads = k) we use: **The General Binomial Probability Formula**:-
          - [n! / (n - k)! * k!] * p^k (1 - p)^(n - k) 

   - **Lesson 23 (Central Limit Theorem):-**
        - It's about the distribution of the sum of many things.
        - **Pascal's Triangle**:-
            - To build the triangle, start with "1" at the top, then continue placing numbers below it in a triangular pattern.
            - Each number is the numbers directly above it added together.
            - Each value is calculated by the sum of the above value + 2 above left value.  
        - if we have large number of experiments and add them up
          - Sum(Xi) from i=1 to n, we get an outcome of a **Gaussian** function. 

   - **Lesson 24 (Central Limit Theorem Programming):-**
        - Some programming about how to create random values of 0 and 1 for specific range
        - compute the mean for that range
        - represent histogram for the range which take the shape of **Bell Curve** which is a Normal Distribution.

   - **Lesson 25 (The Normal Distribution):-**
        - **The General Binomial Probability Formula**:-
          - [n! / (n - k)! * k!] * p^k (1 - p)^(n - k) 
            - n --> number of coin flips
            - k --> number of heads
            - p --> probability of heads
          - we get max value of this expression when k is half n 
        - Normal Distribution Fomula:-
          - N(Xi, M, sig) = (1 / sqrt(2 * π * sig)) * exp {-0.5 * ((Xi - M)^2 / sig)}
          - Where:- 
            - N donates to normal distribution
            - M is the mean
            - sig is the variance
            - π is the pi 
            - exp is exponential function
        - use **Binomial Probability** for few experiments.
        - use **Normal Distributions** for many experiments. 

   - **Lesson 26 (Manipulating Normals):-**
        - When add gaussian variables in normal distribution:-
          - Means add up 
          - Variance add up  
          - Standard deviation don't add up.
        - If X is normal with parameters M and σ^2
          - Then aX + b will have parameters **aM+b** and **a^2σ^2**
        - If you combined X and Y
          - That combined adds up the means **M+M** and varaince **σ^2+σ^2** 
        - If you subtract X and Y
          - That subtraction subtract the means and it will be **0**
          - and adds up the varaince **σ^2+σ^2**  

   - **Lesson 27 (Most Better than Average):-**
        - It's just talking about possible things in statstics  

   - **Lesson 28 (Problem Set 4):-**
        - If you want to calc P(X >= k), you can calc it by: 1- P(X < K) 
        - Exercise about:-
          - Quartile
          - General Binomial Probability
          - Normal Gaussian distribution 
          - Manipulating Normals

   - **Lesson 29 (Programming and Proofs):-**
        - Using quartile to elimnate outlires by keeping items between Q1 and Q3.
        - Proof of mean 
        - Proof of variance
          
   - **Lesson 30 (Confidence Intervals):-**
        - **Confidence Interval** is a range of values we are fairly sure our true value lies in.
            - Usually this range is 95% that the final outcome falls in this range.
        - The more data in sample, the more trust you have.  
          - More Trust --> Smaller Confidence Interval CI
          - Standard deviation **σ** is not affected by the sample size but **CI** is.  
        - Var(aX) = a^2 * Var(X)
        - If mean(X) = P, then Variance(X) σ^2 = P(1-P)  
        - CI =  Mean +/- 1.96 * sqrt(P(1-p) / n )
          - sqrt(P(1-P)) = σ

# What’s new for you ?

   - Quartiles
   - Binomial Distribution
   - Central Limit Theorem
   - Pascal's Triangle 
   - Manipulating Normals

# Additional Resources ? 

   - https://www.mathsisfun.com/data/quartiles.html
   - https://www.mathsisfun.com/data/percentiles.html
   - https://www.mathsisfun.com/data/binomial-distribution.html
   - https://www.mathsisfun.com/pascals-triangle.html
   - https://www.investopedia.com/terms/b/bell-curve.asp#:~:text=A%20bell%20curve%20is%20a%20graph%20depicting%20the%20normal%20distribution,relative%20width%20around%20the%20mean.
   - https://www.mathsisfun.com/data/standard-normal-distribution.html
   - https://en.wikipedia.org/wiki/Normal_distribution
   - https://www.mathsisfun.com/data/standard-deviation.html
   - https://www.mathsisfun.com/data/confidence-interval.html
