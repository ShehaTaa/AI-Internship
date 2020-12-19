# 1- What ’re the methods that you used ?

   1. **String :-**<br />
      - replace
      - slicing

   2. **Time :-**<br />
      - datatime
      - format codes using **strftime**.
      - timedelta
      
   3. **Regular expression :-**<br />
      - re library


# 2- Explain each method ..

   1. **char_count :-**<br />
        Count the number of characters using dictionary and increment<br />
        matching char with 1 using keys as char and numbers as values.
                   
   2. **change_occ_char :-**<br />
        Store first char in var and replace any occurance of<br />
        this var by $ using replace method except first char.
                         
   3. **swap_str :-** <br />
        Swap first 2 char in string with first 2 char in another str<br />
        using slice string.
                  
   4. **add_letters :-**<br />
       Check length of str if > 3 or not
           - if condition match, check last 3 char if ther are ing add ly
           - if they are not ing, add ing
                     
   5. Use **datatime** to get different formate of time using<br />
      **format codes and strftime**  
   
   6. Get **time now** and calc difference with **timedelta with day = 1** as argument 
      to get **time yesterday** by and add **time today + timedalta with day = 1** as argument 
        
   7. Use **timedate** to get time now and add timedelta with **seconds = 5** as argument 
      to calc **time after 5 secends** from now.
      
   8. Use **timedate** to get time now and get start date of the **year 1 / 1 / 2020**
      and calc difference between them to calc **day of year**.
        
   9. Get time and multiply by **1000** to get time in **millisecods**
   
   10. Use **datatime** to get different formate of time using format codes
       and strftime with **"%W"** as argument.
         
   11. - Use **regular expression** to match pattern 
       - *-->Matches **0 or more** occurrences of preceding expression.
       - **$** Matches **end** of line.  
         
   12.  Area of a trapezoid is **area = ((a + b) / 2) * h** <br />
        where a is base 1 and b is base 2 and h is height.
   
 
  

# 3- What’s new for you ?
   - formate codes using strftime     


# 4- Resources ? 
   - https://docs.python.org/3/library/datetime.html#:~:text=A%20timedelta%20object%20represents%20a,between%20two%20dates%20or%20times.&text=All%20arguments%20are%20optional%20and,and%20microseconds%20are%20stored%20internally.
   
   - https://www.w3schools.com/python/python_datetime.asp
   
   - https://www.geeksforgeeks.org/python-datetime-timedelta-function/
   
   - https://www.w3schools.com/python/python_regex.asp
