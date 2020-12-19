# 1- What ’re the methods that you used ?

   - **Regular Expression:-**
        - pattern
        - match() 
        - split()
        - search()
        - groups()
        - compile()
        - match.start() & match.end()
        - findall()
        - re.I

   - **HTML Parser:-**
        - handle_starttag
        - handle_endtag
        - handle_startendtag 
        - handel_comment
        - handle_data
        - feed()

   
   - Fraction()
   - reduce()
   - append
   - map
   - join 
   - format()
   - rstrip()
   - isalnum()



# 2- Explain each method ..

   1. - Given a string S.
      - verify that S is a floating point number under some conditions
      - using regular expression **pattern = r'^[+-]?[0-9]*\.[0-9]+$'**.

   2. - Generate a list of the first N fibonacci numbers, 0 being the first number.
      - Then, apply the map function and a lambda expression to cube each fibonacci number and print the list.
         - cube = lambda x: x ** 3 

   3. - Given a string S consisting only of digits 0-9, commas ,, and dots .
      - Using regex_pattern and re.split() to find all of the , and . symbols in S and split correctly.
         - regex_pattern = r"[.,]"

   4. - Given a string S.
      - Find the first occurrence of an alphanumeric character in S (read from left to right) that has consecutive repetitions.

   5. - Given a list of rational numbers, calculate their product.
      - Using Fraction method and reduce
          - reduce(lambda a, b: a * b, fracs)
          - Fraction(*map(int, input().split())) 

   6. - Given a string S and substring k.
      - Find the indices of the start and end of string k in S.
      - Using:-
          - match.start()
          - match.end()

   7. - Given a text of N lines. The text contains && and || symbols.
      - modify those symbols to the following:
          - && → and
          - || → or
      - Using **re.sub(r'(?<= )(&&|\|\|)(?= )', lambda x: 'and' if x.group() == '&&' else 'or', input())**  

   8. - Given a string S. It consists of alphanumeric characters, spaces and symbols(+,-).
      - find all the substrings of S that contains 2 or more vowels.
      - these substrings must lie in between 2 consonants and should contain vowels only.
      - Using: **r'{Consonants}({Vowels}{{2,}})(?={Consonants})'**

   9. - Given some input, and you are required to check whether they are valid mobile numbers.
      - A valid mobile number is a ten digit number starting with a 7, 8 or 9.
      - Using: **"^[789]\d{9}$"**

   10. - Given N pairs of names and email addresses as input:-
         - print each name and email address pair having a valid email address on a new line.
         - Using: **"^<([a-zA-Z][a-zA-Z0-9\._-]+)@([a-zA-Z]+)\.([a-zA-Z]{1,3})>$"**

   11. - Given lines of CSS code:-
         - Check all valid Hex Color Codes using regular expression to find mathches.
         - print the matched codes
         - Using: **re.findall('#[0-9A-Fa-f]{3,6}', line)**

   12. - Given an HTML code:-
         - print start tags, end tags and empty tags separately.
         - Using HTMLParser and feed method and override HTML Pareser method.
            - handle_starttag
            - handle_endtag
            - handle_startendtag

   13. - Given an HTML code snippet of N lines:-
         - print the single-line comments, multi-line comments and the data.
         - Using HTMLPareser and feed method and override HTML Pareser method
            - handel_comment
            - handle_data  

   14. - Given an HTML code snippet of N lines:-
         - detect and print all the HTML tags, attributes and attribute values.   
         - Using HTMLParser and feed method and override HTML Pareser method.
            - handle_starttag

   15. - create a unique identification number (UID) for each of company employees.
       - A valid UID must follow the rules below:-
         - It must contain at least 2 uppercase English alphabet characters.
         - It must contain at least 3 digits (0 - 9).
         - It should only contain alphanumeric characters (a - z, A - Z & 0 - 9).
         - No character should repeat.
         - There must be exactly 10 characters in a valid UID.

       - Using regular expression:-
         - r'(.*[A-Z]){2,}' 
           - .* matches any character (except for a newline).
           - [A-Z] matches a single character present in the range between A and Z (case sensitive).
         - r'(.*[0-9]){3,}'
           - .* matches any character (except for a newline).
           - [0-9] matches a single character present in the range between 0 and 9 (case sensitive)
         - r'.*(.).*\1+.*'
           - .* matches any character (except for a newline).
           - \1+ matches the same text as the most recently matched by the 1st capturing group.

   16. - Verify whether a credit card numbers are valid or not.
       - Valid credit card has the following characteristics:-
         - It must start with a 4, 5 or 6.
         - It must contain exactly 16 digits.
         - It must only consist of digits (0 - 9).
         - It may have digits in groups of 4, separated by one hyphen "-".
         - It must NOT use any other separator like ' ' , '_', etc.
         - It must NOT have 4 or more consecutive repeated digits.

       - Using rgular expression:-
         - r'^[456]\d{3}(-?)\d{4}\1\d{4}\1\d{4}$' 
           - Check if credit card number size if exactly 16.
           - all the characters are integers.
           - and - symbol may be present after every group of 4 digits.
         - r'(\d)\1{3,}'
           - Check is credit card number has 4 or more repeating consecutive digits.

   17. - Validating Postal Codes.
       - A valid postal code P have to fullfil both below requirements:-
         - must be a number in the range from 100000 to 999999 inclusive.
         - must not contain more than one alternating repetitive digit pair.

       - Using rgular expression:-
         - (?=(\d)\d\1)
           - find how many alternating repetitive digits are there.
         - ^[1-9][0-9]{5}$
           - heck that postal code is in the range 100000 - 999999.
           - Add the boolean obtained from these to checks and print the result. 
       
   18. - Matrix script: 
         - read each column and select only the alphanumeric characters and connect them
         - reads the column from top to bottom and starts reading from the leftmost column.
         - Using regular expression:-
           - r'(\w)(\W+)(\w)'
           - r"\1 \3"

# 3- What’s new for you ?

   - re groups
   - fractions module
   - functools module 
   - HTML Parser

# 4- Resources ? 

   - https://www.w3schools.com/python/python_regex.asp
   - https://www.programiz.com/python-programming/regex
   - https://en.wikipedia.org/wiki/Fibonacci_number
   - https://www.geeksforgeeks.org/functools-module-in-python/
   - https://docs.python.org/3/library/functools.html
   - https://docs.python.org/3/library/fractions.html
   - https://www.tutorialspoint.com/Why-do-we-use-re-compile-method-in-Python-regular-expression
   - https://docs.python.org/2/library/re.html#re.sub
   - https://en.wikipedia.org/wiki/Parsing
   - https://docs.python.org/2/library/htmlparser.html#HTMLParser.HTMLParser



