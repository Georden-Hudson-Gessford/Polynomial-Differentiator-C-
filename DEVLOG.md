
For Versions 1-3





Version 4 and beyond 
6-17-26
The strategy for decomposition will be to handle cases with their own function. 
Constants may have a function, polynomial terms, trigonometric functions. 
That function will return it and build into the string. 

7-3-26
finish by 7-15-26 with chain rule and trigonometric implementation
* Added a function to detect parentheses. This will be useful for detecting chain rule.
* (Because terms are split by either + or -, any inner function containing signs must not be confused for a new term
* EX: (5x+4+3)^2
* So I will have the termsplitting function ignore information squeezed between parentheses

  7-4-26
  Created function to find all +,-
  
  7-6-26
  Created 2 functions to eliminate signs that are not seperating terms (in parentheses and after exponents ^ )
  Setup debugging and test cases as two separate text files. Will start 3rd text file to document bug history.
  I need to do a little cleanup work in my code, also make seperate files if i remember how to do that.
  It would also be easy if there is a way to run multiple test cases.
  Using functions as debuggers will organize what i am printing, bools can also be used so i can enter and exit debug mode for different functions
  A vector list for test cases
  Next create a file for the parsing process, another file for debugging and  another that can run test cases. ++

7-7-26
I have created proper header files and will have a main file, parser file, and differentiator file.
Created a function to split terms
I have made the decision that expressions the calculator cannot handle will be pruned instead of shutting down
these will include cases such as csc(x), a^x, (sin(x)^-1, arcsin(x), logs, products, division (even if not quotient rule), fractional or decimal coefficients
Also includes unsimplified expressions such as 4^3 or 500(3x^2)^4. 
I think chain rule will be treated recursively



7-8
  * I am looking to move slower with the pruning function
  * It requires a great deal of recursion i am unfamiliar with  and is on a scale i have yet to deal with
  * I am going to move slower with this process and take time to learn better structures and a way to analyze before it becomes catastrophic.

7-8
  * I am aiming to combine functions and minimize code
  * Prevent copying strings of vectors when i implement recursion
  * Utilize a depth counter for nesting
  * tokenization
  * Full overview before continuing and resume programming beyond today.
