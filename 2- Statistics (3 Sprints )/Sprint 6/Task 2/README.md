# 1- What ’re the methods that you used ?

   - combinations
   - random
   - scipy.stats.pearsonr
   - sqrt
   - round
   - math.erf
   - scipy.stats.poisson



# 2- Explain each method ..

   1. **Basic Probability Puzzles 5**
        - There are 10 people about to sit down around a round table.
        - Find the probability that 2 particular people will sit next to one another.
        - Sol:-
          - One person will sit, leaving nine positions.
          - Each position has two seats, one on the left side and one on the right side.
          - define a combination with length 2
          - iterate through it and check condition
            - if (e[1] - e[0] == 1) or (e[0] == 0 and e[1] == 9)

   2. **Basic Probability Puzzles 6**
        - Bag X contains 5 white balls and 4 black balls.
        - Bag Y contains 7 white balls and 6 black balls.
        - You draw 1 ball from bag X and, without observing its color, put it into bag Y.
        - Now, if a ball is drawn from bag Y, find the probability that it is black.
        - Sol:-
          - P(Y = b | X = w) * P(X = w) + P(Y = b | X = b) + P(X = b) 

   3. **Basic Probability Puzzles 7**
        - A firm produces steel pipes in three plants.
          - Plant A produces 500 units per day and has a fraction defective output of 0.005.
          - Plant B produces 1000 units per day and has a fraction defective output of 0.008.
          - Plant C produces 2000 units per day and has a fraction defective output of 0.010.
        - At random, a pipe is selected from the day’s total production and it is found to be defective.
        - What is the probability that it came from plant A?  
        - Sol:- 
          - compute total probability of each firm
          - Then divide join probability of firm A by sum of all join probability. 

   4. **Basic Probability Puzzles 9**
        - A candidate is selected for interview of management trainees for 3 companies.
          - For the first company, there are 12 candidates
          - For the second there are 15 candidates
          - and for the third, there are 10 candidates.
          - Find the probability that he is selected in at least one of the companies.
        - Assume that 1 candidate will be selected in each of the interviews, and all candidates appearing for the interview have an equal probability of getting selected.
   
        - Sol:-
          - Probabilites for getting each job: 1/12, 1/15, 1/10
          - These are the following states (0 means did not get that job and 1 means got that job)
            - 000
            - 001
            - 010
            - 011
            - 100
            - 101
            - 110
            - 111
          - So, we calc 1 - ~P(A)~P(B)~P(C)  

   5. **Basic Probability Puzzles 10**
        - Bill and Nina appear for an interview for two vacancies.
        - The probability of Bill’s selection is 1/3 and that of Nina’s selection is 1/5.
        - Find the probability that only one of them will be selected.
        - Sol:-
          - p(B) to be selected = 1/3 =, so p(~B) to be not selected = 2/3
          - p(N) to be selected = 1/5 =, so p(~N) to be not selected = 4/5
          - we mul p(B) * 1-p(N) + p(N) * 1-p(B)
          - probability that only one of them will be selected = 1/3 * 4/5 + 1/5 * 2/3 = 2/5

   6. **Correlation and Regression Lines 1**

        - For a particular scatter plot, the line of regression of y on x is:
          - 3x + 4y + 8 = 0 
        - And the line of regression of x on y is:
          - 4x + 3y + 7 = 0
        - Find the Pearson Product moment coefficient,r , correct to a scale of 2 decimal places.
        - Sol:-
          - we calc y from equations.
          - Then we call pearsonr method from scipy library to calc Pearson Product moment coefficient, r
          - pearsonr(x, y) --> r - float Pearson’s correlation coefficient

   7. **Correlation and Regression Lines 2**

        - There are 2 series of data involving index numbers: P for price index and S for the commodity stock.
        - The mean and standard deviation of P are 100 and 8, respectively.
        - The mean and standard deviation of S are 103 and 4, respectively.
        - The  R^2 correlation coefficient between the two series is 0.4.
        - With this data, obtain the slope of the regression line of P on S, correct to a scale of 2 decimal places.
        - Sol:-
          - r = cov(x,y)/sd(x)/sd(y)
          - r^2 = R^2
          - slope = cov(x, y) / var(x)
          - R^2 = slope^2 * var(x)^2 / sd(x)^2 / sd(y)^2

   8. **Correlation and Regression Lines 3**

        - The two regression lines of a bivariate distribution are:
          - 4x – 5y + 33 = 0 
          - 20x – 9y – 107 = 0
        - Calculate the arithmetic means of x and y respectively. (Both of these are integer values.)
        - Sol:-
          - from eq1 we get x = 5/4 y - 33/4   --> 1
          - from eq2 we get y = 20/9 x - 107*9 --> 2
          - b = y_mean - slope * x_mean
            - slope from 1 = -5/4 and b = -33/4
            - slope from 2 = 20/9 and b = -107/9
          - so, we got:
            - -33/4  = x_mean - 5/4 y_mean
            - -107/9 = y_mean - 20/9 x_mean
          - slove the two equations
            - **X_mean = 13 and Y_mean = 17**

   9. **The Central Limit Theorem 1**

        - A large elevator can transport a maximum of 9800 pounds.
        - Suppose a load of cargo containing 49 boxes must be transported via the elevator.
        - The box weight of this type of cargo follows a distribution with:
          - a mean of µ = 208 pounds
          - a standard deviation of 15 pounds. 
        - Based on this information, what is the probability that all  boxes can be safely loaded onto the freight elevator and transported?
        - sol:-
          - define a function that calculate z score and return the probability according to CLT formula.
            - 0.5 * (1 + math.erf((x - mean) / (sd * (2 ** 0.5))))

   10. **The Central Limit Theorem 2**

        - The number of tickets purchased by each student for the University X vs.
        - University Y football game follows a distribution that has:
          - a mean of µ = 2.4
          - a standard deviation of σ = 2.0.
        - Suppose that a few hours before the game starts, there are 100 eager students standing in line to purchase tickets.
        - If there are only 250 tickets left, what is the probability that all 100 students will be able to purchase the tickets they want? 
        - Sol:-
          - define a function that calculate z score and return the probability according to CLT formula.  
            - 0.5 * (1 + math.erf((x - mean) / (sd * (2 ** 0.5))))

   11. **The Central Limit Theorem 3**

        - You have a sample of 100 values from a population with mean µ = 500 and with standard deviation σ = 80.
        - What is the probability that the sample mean will be in the interval (490, 510)? 
        - Sol:-
          - define a function that calculate z score and return the probability according to CLT formula. 
          - Calculate p1 of 490 and p2 of 510 and subtract p2 from p1 
            - 0.5 * (1 + math.erf((x - mean) / (sd * (2 ** 0.5))))

   12. **The Central Limit Theorem 4**

        - You have a sample of 100 values from a population with
          - Mean µ = 500
          - standard deviation σ = 80.
        - Compute the interval that covers the middle 95% of the distribution of the sample mean.
          - i.e, compute and such that P( < x < ) = 0.95
        - Sol:-
          - Given values:- 
            - n = 100
            -  µ = 500
            - σ_sampl = 80 / √n
            -  z = 1.96   
          - we compute interval 1:-
            - sample_mu - zed * sample_sigma
          - interval 2:-
            - sample_mu + zed * sample_sigma
   
   13. **The Central Limit Theorem 5**

        - The amount of regular unleaded gas purchased every week at a particular gas station follows the normal distribution with:-
          - a mean of 50000 gallons
          - a standard deviation of 10000 gallons.
        - The starting supply of gasoline is 74000 gallons, and there is a scheduled weekly delivery of 47000 gallons.   
        - Compute the probability that, after 11 weeks, the supply of gasoline will be below 20000 gallons.
        - Sol:-
          - Given values:-
            - mu = 50000
            - sigma = 10000
            - weeks = 11
            - start = 74000
            - weekly = 47000
          - we compute:-
            - end = start + weekly * weeks
            - lower_bound = end - 20000
            - sum_mu = weeks * mu
            - sum_sigma = weeks ** 0.5 * sigma   
          - define a function that calculate z score and return the probability according to CLT formula. 
            - 0.5 * (1 + math.erf((x - mean) / (sd * (2 ** 0.5)))) 

   14. **The Central Limit Theorem 6**

        - The amount of regular unleaded gas purchased every week at a particular gas station follows the normal distribution with:-
          - a mean of 50000 gallons
          - a standard deviation of 10000 gallons.
        - The starting supply of gasoline is 74000 gallons, and there is a scheduled weekly delivery of 47000 gallons. 
        - How many gallons should the weekly delivery be so that after 11 weeks the probability that the supply is below 20000 gallons is only 0.5%?
        - Sol:-
          - Given values:- 
            - mu = 50000
            - sigma = 10000
            - weeks = 11
            - start = 74000
            - weekly = 47000
            - end = start + weekly * weeks
            - lower_bound = end - 20000
            - sum_mu = weeks * mu
            - sum_sigma = weeks ** 0.5 * sigma
          - Let A be the unknown schedule delivery  
          - The total gasoline purchased must be more than 74000 + 11 A - 20000 
          - P(T > 74000 + 11 A - 20000) = 0.005 
          - z-value that corresponds to this probability is 2.575
          - 2.575 = start + weeks * A - 20000 - sum_mu / sum_sigma 
          - A = 52854.8  
 
   15. **Poisson Distribution 1**

        - **Poisson Distribution:**
            - is a discrete probability distribution that expresses the probability of a given number of events occurring in a fixed interval of time or space if these events occur with a known constant mean rate and independently of the time since the last event.
        - A random variable X follows Poisson distribution with mean 2.5.
        - Find the probability with which the random variable X is equal to 5; i.e. P(X = 5).
        - Sol:-
          - we call poisson scipy.stats to compute the prob of x = 5 
          - poisson.pmf(x, mu) 
            - x = 5, mu = 2.5

   16. **Poisson Distribution 2**

        - The manager of a industrial plant is planning to buy a machine of either type A or type B.
        - For each day’s operation the number of repairs X, that the machine A needs is a poisson random variable with mean **0.88**.
        - The daily cost of operating A is
          - **CA = 160 + 40 ∗ X^2**
        - For machine B, let Y be the poisson random variable indicating the number of daily repairs, which has mean **1.55**.
        - The daily cost of operating B is
          - **CB = 128 + 40 ∗ Y^2**
        - Assume that the repairs take negligible time and each night the machine are cleaned so that they operate like new machine at the start of each day.
        - What is the expected daily cost of each machine ? 
        - Sol:-
          - mean_A = 0.88
          - mean_B = 1.55
          - C_A = 160 + 40*(mean_A + mean_A^2)
          - C_B = 128 + 40*(mean_B + mean_B^2)

   17. **Standard Deviation Puzzles 1**

        - Find the largest possible value of N where
          - the standard deviation of the values in the set {1,2,3,N} is equal to the standard deviation of the values in the set {1,2,3}.
          - Output the value of N, correct to two decimal places.
          - Sol:-
            - Compute stdev of l1 
            - compute stdev of l2
            - then we comapre between stdev1 and stdev2
              - if round(sd1, 3) == round(sd2, 3):
                - round(N, 2)

   18. **Standard Deviation Puzzles 2**

        - The heights of a group of children are measured.
        - The resulting data has a mean of 0.675 meters, and a standard deviation of 0.065 meters.
        - One particular child is 90.25 centimeters tall.
        - Compute z, the number of standard deviations away from the mean that the particular child is.   
        - Sol:-
          - z = (x - mu)/sd

   19. **Standard Deviation Puzzles 3**

        - Let X and Y be two independent "normal" random deviates with
          - mean of 10, 3
          - and standard deviation of  20 , 4.
        - Let  be the value of the standard deviation of the distribution obtained by
          - adding the two distributions (X + Y).
        - In the answer box, enter the value of σ, correct to one place of decimal. 
        - Sol:-
          - math.sqrt(sd1^2 + sd2^2) 

   20. **Standard Deviation Puzzles 4**
 
        - Let X and Y be two independent "normal" random deviates with:-
          - mean of 10 and 3
          - standard deviation of 20 and 4
        - Let σ be the value of the standard deviation of the distribution obtained by computing the difference of the two distributions (X - Y).
        - find the value of σ, correct to one place of decimal.
        - Sol:-
          - math.sqrt(sd1^2 + sd2^2)
 
# 3- What’s new for you ?

   - Pearson’s correlation coefficient
   - Poisson Distribution

# 4- Resources ? 

   - https://win-vector.com/2011/11/21/correlation-and-r-squared/
   - https://www.khanacademy.org/math/ap-statistics/bivariate-data-ap/assessing-fit-least-squares-regression/v/r-squared-or-coefficient-of-determination
   - https://www.khanacademy.org/math/probability/statistics-inferential/sampling-distribution/v/sampling-distribution-example-problem
   - https://www.phptpoint.com/python-math-erf-method/
   - https://www.statisticshowto.com/probability-and-statistics/normal-distributions/central-limit-theorem-definition-examples/
   - https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.poisson.html
   - https://www.statisticshowto.com/poisson-distribution/
   - https://en.wikipedia.org/wiki/Poisson_distribution
   - http://www.stat.ucla.edu/~nchristo/statistics100A/stat100a_clt.pdf
