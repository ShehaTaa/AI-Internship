# 1- What ’re the methods that you used ?

   - **cmath library:-**
        - polar()  
   
   - **math library:-**
        - atan()
        - degrees()
   
   - divmod() 
 
   - mod power
        - pow(x, y, z)


# 2- Explain each method ..

   1.  Polar coordinates give an alternative way to represent a complex number
        1. input a complex number like 1+2j
        2. use polar method to convert it to polar coordinates
        3. print modulus r and phase phi
 
   2. In triangle ABC:-
        - ABC is a right triangle 90 at B
        - M is the midpoint of AC so, AM = MC
        - so, from that BM = MC = AM, and from that
            angle MBC = angle ACB
        - so, we calc angle ACB using nverse tangent atan(x)
        - note that, we calc Ac from Pythagorean Theorem as 
             AC = math.sqrt(AB^AB, BC^BC)
        <br />
        1. so, i use math atan method to get the angle between AB and BC.<br />
        2. then use math degrees to converts angle from radians to degrees.<br />
        3. then use round method to get rounded number

   3. Print a trinagle quest given integer N
        - using logic = (pow(10 , i) // 9) ** 2

   4. Print divmod result
        - using divmod python method
        - syntax of divmod() is:-
            - divmod(x, y)
       
        - divmod() takes two parameters:-
            - x --> a non-complex number (numerator)
            - y --> a non-complex number (denominator)
       
        - divmod() returns:-
            -(q, r) - a pair of numbers (a tuple) consisting of
              quotient q and remainder r
            - If x and y are integers, the return value from divmod()
              is same as (a // b, x % y).
            - If either x or y is a float, the result is (q, x%y).<br />
              Here, q is the whole part of the quotient.    

   5. Using mod power to print the (pow(x,y)) % z :-<br />
        - pow() Parameters:-<br />
            - The pow() function takes three parameters:-<br />
                - x --> a number, the base<br />
                - y --> a number, the exponent<br />
                - z (optional) --> a number, used for modulus<br />
            - pow(x, y) is equal to pow(x,y)
            - pow(x, y, z) is equal to (pow(x,y)) % z 
        
   6. given 4 integer numbers a, b, c, and c, calculate **(pow(a,b) + pow(c,d)**
  
   7. Print a trinagle quest given integer N
        - using logic = (pow(10 , i) // 9) * i 


# 3- What’s new for you ?
  
   - cmath library
   - math library 
        - atan()
        - degrees()
   - mod power
   - divmod() 


# 4- Resources ? 

   - https://ocw.mit.edu/courses/mathematics/18-01-single-variable-calculus-fall-2006/video-lectures/lecture-32-polar-coordinates/
   - https://www.w3schools.com/python/module_cmath.asp
   - https://docs.python.org/3/library/cmath.html
   - https://www.w3schools.com/python/ref_cmath_phase.asp
   - https://www.w3schools.com/python/ref_cmath_polar.asp
   - https://www.journaldev.com/23435/python-complex-numbers-cmath
   - https://www.programiz.com/python-programming/methods/built-in/round
   - https://www.mathopenref.com/arctan.html
   - https://www.w3schools.com/python/ref_math_atan.asp
   - https://www.programiz.com/python-programming/methods/built-in/pow
  
