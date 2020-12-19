# 1- What ’re the methods that you used ?

   - **xml.etree.ElementTree:-**
        - ElementTree() 
        - fromstring()
        - node.attrib
        - getroot()
    
   - Python decorator 

   - **Python numpy:**
        - array()
        - reshape()
        - transpose()
        - flatten()
        - concatenate()
        - ones()
        - zeros()
        - eye()
        - add()
        - subtract()
        - multiply()
        - mod()
        - power()
        - floor()
        - ceil()
        - rint()
        - prod()   
        - sum()
        - max()
        - min()
        - mean()
        - var()
        - std()
        - dot()
        - inner()
        - outer()
        - polyval()
        - det() 
    
   - join()
   - sorted()
   - range()
   - split()
   - map()

# 2- Explain each method ..

   1. - Given a valid XML document, print its score.
      - The score is calculated by the sum of the score of each element.
      - For any element, the score is equal to the number of attributes it has.
        - So, I use ElementTree fromstring to convert inputed string to XML 
        - and use node.attrib to get attribute of each element.
        - Then sum the number of attributes in XML
 
   2. - Given a valid XML document, print the maximum level of nesting in it.
      - Take the depth of the root as 0.
         - So, I build a depth func that take element and level as arguments
         - and check the maxdepth of our xml
           - if  if level == maxdepth: maxdepth += 1
         - then loop for other element and call depth func recursively, and increase level by 1 

   3. - Given N mobile numbers.
      - Sort them in ascending order then print them in the standard format shown below: +91 xxxxx xxxxx  
        - So, Using decorator, I build a wrapper func that take func as argument
        - inside wrapper, i define another funk that take a list of number as argument
           - loop through number and use slice to handel it
             - [::-1] --> reverse list number 
             - [0:10] --> selcet first 10 number in reversed list to git rid of any additionl number
             - [::-1] --> reverse the list number again after gitting rid of any additionl number

        - and then use sort_phone func to sort the number in  ascending order

   4. - Given some information about N people.
        - Each person has a first name, last name, age and sex.
        - Print their names in a specific format sorted by their age in ascending order i.e.
        - The youngest person's name should be printed first.
        - For two people of the same age, print them in the order of their input.
        - So, Using decorator, I build a person_lister func that take another func as argument
        - inside person_lister func, i define another func inner which take people info as argument
          - inner func sort people according to age
          - then, put the sorted formated people in a list 
        - name_format func, return the formatted person name to be printed.     
  
   5. - Consider that vowels in the alphabet are a, e, i, o, u and y.
      - Function score_words takes a list of lowercase words as an argument and returns a score as follows:
        - The score of a single word is 2 if the word contains an even number of vowels.
        - Otherwise, the score of this word is 1.
        - The score for the whole list of words is the sum of scores of all words in the list.

   6. - Given a space separated list of numbers.
      - Task is to print a reversed NumPy array with the element type float. 
        - Using: np.array(arr[::-1], float) 

   7. - Given a space separated list of nine integers.
      - Task is to convert this list into a 3 X 3 NumPy array.
        - Using: np.array(arr, int).reshape(3, 3)

   8. - For each keyword argument of a function, we can assign a default value  
      - which is going to be used as the value of said argument if the function is called without it. 
      - So, i have defined print_from_stream func which take 2 arguments 
        - (n, stream = None) --> default stream argument = None
        - then loop through range to get the next item in the specific stream

   9. - Given a X integer array matrix with space separated elements ( = rows and = columns).
      - Task is to print the transpose and flatten results. 
        - Using: 
           - arr = numpy.array(lines) 
           - numpy.transpose(arr)
           - arr.flatten()

  10. - Given two integer arrays of size N X P and M X P (N & M are rows, and P is the column).
      - Task is to concatenate the arrays along axis 0.
        - Using: numpy.concatenate((arr1, arr2), axis = 0)

  11. - Given the shape of the array in the form of space-separated integers
      - each integer representing the size of different dimensions
      - Task is to print an array of the given shape and integer type using the tools numpy.zeros and numpy.ones.
        - Using: - np.zeros(N, dtype = numpy.int)
                 - np.ones(N, dtype = numpy.int)

  12. - Task is to print an array of size N X M with its main diagonal elements as 1's and 0's everywhere else. 
        - Using: np.eye(N, M, k = 0)

  13. - given two integer arrays, A and B of dimensions N X M.
      - Task is to perform the following operations:
         - Add (A + B) using: numpy.add(A,B)
         - Subtract (A - B) using: numpy.subtract(A,B)
         - Multiply (A * B) using: numpy.multiply(A,B)
         - Integer Division (A / B) using: 
         - Mod (A % B)
         - Power (A ** B)

  14. - Given a 1-D array, A.
      - Task is to print the Floor, Ceil and Rint of all the elements of A. 
        - Using: 
           - np.floor(arr)
           - np.ceil(arr)
           - np.rint(arr)

  15. - Given a 2-D array with dimensions N X M.
      - Task is to perform the sum tool over axis 0 and then find the product of that result.
        - Using: np.prod(np.sum(nparr, axis = 0))

  16. - Given a 2-D array with dimensions N X M.
      - Task is to perform the min function over axis 1 and then find the max of that.
        - Using: np.max(numpy.min(nparr, axis = 1))

  17. - Given a 2-D array of size N X M.
      - Task is to find:
        - The mean along axis 1 using: np.mean(nparr, axis = 1)
        - The var along axis 0 using: np.var(nparr, axis = 0)
        - The std along axis None using: np.std(nparr, axis = None)

  18. - Given two arrays A and B. Both have dimensions of N X N.
      - Task is to compute their matrix product.
        - Using: np.dot(A, B)

  19. - Given two arrays: A and B.
      - Task is to compute their inner and outer product.
        Using: - np.inner(A, B)
               - np.outer(A, B)

  20. - Given the coefficients of a polynomial P.
      - Task is to find the value of P at point x.
        - Using: np.polyval(m, n)

  21. - given a square matrix A with dimensions N X N.
      - Task is to find the determinant.
        - Using: round(np.linalg.det(matrix),2)
 
# 3- What’s new for you ?

   - Python XML
   - numpy inner and outer


# 4- Resources ? 

   - https://docs.python.org/3/library/xml.etree.elementtree.html#xml.etree.ElementTree.fromstring
   - https://docs.python.org/3/library/xml.etree.elementtree.html#xml.etree.ElementTree.ElementTree
   - https://docs.python.org/3/library/xml.etree.elementtree.html
   - https://docs.python.org/3/library/xml.etree.elementtree.html#xml.etree.ElementTree.XMLParser
   - https://diveintopython3.net/xml.html
   - http://simeonfranklin.com/blog/2012/jul/1/python-decorators-in-12-steps/
   - https://www.programiz.com/python-programming/decorator
   - https://www.programiz.com/python-programming/closure
   - https://railsware.com/blog/python-for-machine-learning-indexing-and-slicing-for-lists-tuples-strings-and-other-sequential-types/
   - https://numpy.org/doc/stable/reference/generated/numpy.reshape.html?highlight=reshape#numpy.reshape
   - https://numpy.org/doc/stable/reference/generated/numpy.concatenate.html
   - https://numpy.org/doc/stable/reference/generated/numpy.zeros.html?highlight=zeros#numpy.zeros
   - https://numpy.org/doc/stable/reference/generated/numpy.eye.html
   - https://numpy.org/doc/stable/reference/generated/numpy.identity.html
   - https://www.geeksforgeeks.org/numpy-mod-in-python/
   - https://www.geeksforgeeks.org/numpy-power-python/
   - https://www.geeksforgeeks.org/numpy-add-in-python/#:~:text=add()%20function%20is%20used,not%20same%2C%20that%20is%20arr1.
   - https://www.geeksforgeeks.org/numpy-subtract-in-python/
   - https://www.geeksforgeeks.org/numpy-multiply-in-python/
   - https://numpy.org/devdocs/user/basics.types.html
   - https://numpy.org/doc/stable/reference/generated/numpy.floor.html
   - https://numpy.org/doc/stable/reference/generated/numpy.ceil.html
   - https://numpy.org/doc/stable/reference/generated/numpy.rint.html
   - https://numpy.org/doc/stable/reference/generated/numpy.maximum.html
   - https://numpy.org/doc/stable/reference/generated/numpy.ndarray.min.html
   - https://numpy.org/doc/stable/reference/generated/numpy.sum.html
   - https://numpy.org/doc/stable/reference/generated/numpy.outer.html
   - https://numpy.org/doc/stable/reference/generated/numpy.inner.html
   - https://www.tutorialspoint.com/numpy/numpy_inner.htm
   - https://numpy.org/doc/stable/reference/generated/numpy.polyval.html
   - https://numpy.org/doc/stable/reference/generated/numpy.linalg.det.html









