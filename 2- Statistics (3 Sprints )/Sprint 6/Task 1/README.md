# 1- What ’re the methods that you used ?

   - range()
   - for() 
   _ if()

# 2- Explain each method ..

   1. In a single toss of 2 fair (evenly-weighted) 6-sided dice
        - find the probability of that their sum will be at most 9. 
        - It's 30/36 for [(1,1),(1,2),(1,3),(1,4),(1,5),(1,6),<br />
                          (2,1),(2,2),(2,3),(2,4),(2,5),(2,6),<br />
                          (3,1),(3,2),(3,3),(3,4),(3,5),(3,6),<br />
                          (4,1),(4,2),(4,3),(4,4),(4,5),<br />
                          (5,1),(5,2),(5,3),(5,4),<br />
                          (6,1),(6,2),(6,3)]
 
        - Create 2 loops for the two dice
          - Verify that sum will be at most 9 using:-
            - if (i + j) <= 9:
          - Then add probability to result using:-
            - result += probability ** 2

   2. For a single toss of 2 fair (evenly-weighted) 6-dice
        - find the probability that the values rolled by each die will be different and their sum is 6.
        - It's 4/36 for[(1,5),(2,4),(4,2),(5,1)] 
        - Create 2 loops for the two dice
          - Verify if each die will be different and their sum is 6 using:-
            - (i != j) and (i + j) == 6:
          - Then add probability to result using:-
            - result += probability ** 2

   3. There are 3 urns: X, Y and Z.
        - Urn X contains 4 red balls and 3 black balls.
        - Urn Y contains 5 red balls and 4 black balls.
        - Urn Z contains 4 red balls and 4 black balls.
        - One ball is drawn from each urn. 
        - What is the probability that the 3 balls drawn consist of 2 red balls and 1 black ball? 
        - Sol:-
          - **Combinations:-**
               X	  Y	     Z
              red	 red	   black
             black	 red	    red
              red	black	    red
        - So, We have three different combinations

   4. Basic Probability Puzzles 4
        - Bag 1 contains 4 red balls and 5 black balls.
        - Bag 2 contains 3 red balls and 7 black balls.
        - One ball is drawn from the Bag 1, and 2 balls are drawn from Bag 2.
        - Find the probability that 2 balls are black and 1 ball is red.
        - Sol:-

              Bag1     Bag2      Bag2
              black    black     red
              black    red       black
              red      black     black
 
   5. Standard Deviation Puzzles - 5
        - If 10 points were added to each of the 500 scores in a sample having:-
          - a mean of 45 and standard deviation of 10
          - The new value of the standard deviation for the sample would be?
          - Sol:-
            - If we add fixed value to scores, new mean will be 55
            - std will remane the same as 10 because the spread of the data remain same.

   6. Standard Deviation Puzzles - 6
        - If we double (multiply by 2) each of the 500 scores in a sample having:-
          - a mean of 45 and standard deviation of 10
          - The new value of the standard deviation for the sample would be ?
          - Sol:-
            - if we mul every value by 2 so new mean will also mul by 2
            - new mean = 45 * 2 = 90
            - new std will be 10 * 2 = 20 

# 3- What’s new for you ?

   - Review on bascis probability   

# 4- Resources ? 

   - http://pi.math.cornell.edu/~mec/2008-2009/TianyiZheng/Bayes.html
   - https://mathworld.wolfram.com/CircularPermutation.html
