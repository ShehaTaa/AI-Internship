# 1- What ’re the methods that you used ?
 
   - scipy.stats.poisson.pmf
   - scipy.stats.poisson.cdf

# 2- Explain each method ..

   1. **Poisson Distribution 3**

        - The number of calls coming per minute into a hotels reservation center is Poisson random variable with mean 3.
        - (a) Find the probability that no calls come in a given 1 minute period.
        - (b) Assume that the number of calls arriving in two different minutes are independent.
          - Find the probability that at least two calls will arrive in a given two minute period.
        - Sol:-
          - scipy.stats.poisson.pmf(0,3)
          - 1-scipy.stats.poisson.cdf(1, 3*2)

   2. **Poisson Distribution 5**
 
        - The number of misprints on a page of The Economic Times has a Poisson distribution with mean 1.2.
        - Find the probability that the number of errors:-
          - on page 10 is 2
          - on page 1 is less than 3 
          - on first ten pages totals 5
          - on all forty pages adds up to at least 3. 
        - Sol:-
          - scipy.stats.poisson.pmf(2, 1.2)
          - scipy.stats.poisson.cdf(2, 1.2)
          - scipy.stats.poisson.pmf(5, 1.2*10)
          - 1-scipy.stats.poisson.cdf(2, 1.2*40)

   3. **Basic Probability Puzzles 8**

        - In a certain city, the probability of a resident not reading the morning newspaper is 1/2
        - and the probability of a resident not reading the evening newspaper is 2/5.
        - The probability they will read both newspapers is 1/5.
        - Find the probability that a resident reads a morning or evening newspaper.
        - Sol:-
          - p(not reading morn) = 1/2
          - p(reading morn) = 1/2
          - p(not reading even) = 2/5
          - p(reading even) = 3/5
          - P(reading both) = 1/5
          - **p(reading morn or even)** = p(reading morn) + p(reading even) - p(reading both)
                              = 1/2 + 3/5 - 1/5

# 3- What’s new for you ?

   - poisson.cdf
   - poisson.pmf
   - Poisson distribution

# 4- Resources ? 

   - https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.poisson.html
   - https://en.wikipedia.org/wiki/Poisson_distribution
   - https://brilliant.org/wiki/poisson-distribution/#:~:text=The%20Poisson%20distribution%20is%20the,the%20drive%2Dthrough%20per%20minute.
   - https://www.youtube.com/watch?v=jmqZG6roVqU
