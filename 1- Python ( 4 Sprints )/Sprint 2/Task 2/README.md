# 1- What ’re the methods that you used ?
   - List Comprehensions
   - Loops and condition statement
   - dictionary
     - split
     - map
     - format
   - hash method
   - set

# 2- Explain each method ..
   1. - Enter three integers x, y, and z representing the dimensions of a cuboid along with an integer n
      - cast the input from x, y, z to int.
      - loop through the 3 values of x, y, z and check if sum of x + y + z != n, print list of three values.
        as [i, j, k] where i value of x, j value of y, and k value of z
        
   2. - Given the names and grades for each student in a class of n students, store them in a nested list
      - and print the name(s) of any student(s) having the second lowest grade.   
        1. So, i take the number of student from user.
        2. Then take name of stu and it's score and store them in list
        3. Store scores of students in a list
        4. Then sort the list and store second high score in var
        5. Then return name of student that match this score
        
   3. - Read in a dictionary containing key/value pairs of name:[marks] for a list of students 
      - and then Print the average of the marks array for the student name provided, showing 2 places after the decimal.  
        1. So, i take the number of student from user.
        2. Initilize student_marks as dictionary
        3. Then take stu name and scores in one line and 
           split them as name and *scores
        4. Split the scores in the marks and store them in a list  
        5. Assign scores to each student
        6. Make query by name and calc score avg for stu name selected
        
   4. Make some operations on list:-
        - define a func take 2 params, empty list, operations and values as one line
        - use if else statement to check every condition and execute the right entered op
        
   5. - Given an integer,n, and n space-separated integers as input, create a tuple, t, of those n integers.
      - Then compute and print the result of **hash(t)**.
        - The hash() method returns the hash value of an object if it has one.
        - Hash values are just integers that are used to compare dictionary keys during a dictionary lookup quickly.
        - Internally, hash() method calls __hash__() method of an object which is set by default for any object.
        - The syntax of hash() method is:-
           - hash(object)  
        - hash() Parameters
          - hash() method takes a single parameter:-
          - object --> the object whose hash value is to be returned (integer, string, float)  
          
   6. Select the score before the last:-
       - use set to prevent duplicate scores
       - use sorted to sort in ascending order to get The score before the last
    

# 3- What’s new for you ?
   - hash method
   - The * is being used to grab additional returns from the split statement


# 4- Resources ?
  
   - https://codereview.stackexchange.com/questions/132381/hackerrank-lists-code
   - https://docs.python.org/3/library/functions.html#hash
   - https://stackoverflow.com/questions/49416732/exclude-builtin-module
   - https://www.programiz.com/python-programming/methods/built-in/hash
