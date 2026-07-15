
For Versions 1-3





Version 4 and beyond 
6-17-26
* The strategy for decomposition will be to handle cases with their own function. 
* Constants may have a function, polynomial terms, trigonometric functions. 
* That function will return it and build into the string. 

7-3-26
*finish by 7-15-26 with chain rule and trigonometric implementation
* Added a function to detect parentheses. This will be useful for detecting chain rule.
* (Because terms are split by either + or -, any inner function containing signs must not be confused for a new term
* EX: (5x+4+3)^2
* So I will have the termsplitting function ignore information squeezed between parentheses

  7-4-26
  *Created function to find all +,-
  
  7-6-26
  * Created 2 functions to eliminate signs that are not seperating terms (in parentheses and after exponents ^ )
  * Setup debugging and test cases as two separate text files. Will start 3rd text file to document bug history.
  * I need to do a little cleanup work in my code, also make seperate files if i remember how to do that.
  * It would also be easy if there is a way to run multiple test cases.
  * Using functions as debuggers will organize what i am printing, bools can also be used so i can enter and exit debug mode for different functions
  * A vector list for test cases
  * Next create a file for the parsing process, another file for debugging and  another that can run test cases. ++

7-7-26
* I have created proper header files and will have a main file, parser file, and differentiator file.
* Created a function to split terms
* I have made the decision that expressions the calculator cannot handle will be pruned instead of shutting down
* these will include cases such as csc(x), a^x, (sin(x)^-1, arcsin(x), logs, products, division (even if not quotient rule), fractional or decimal coefficients
* Also includes unsimplified expressions such as 4^3 or 500(3x^2)^4. 
* I think chain rule will be treated recursively



7-8
  * I am looking to move slower with the pruning function
  * It requires a great deal of recursion i am unfamiliar with  and is on a scale i have yet to deal with
  * I am going to move slower with this process and take time to learn better structures and a way to analyze before it becomes catastrophic.

7-8
  * I am aiming to combine functions and minimize code
  * Prevent copying strings of vectors when i implement recursion
  * Utilize a depth counter for nesting
  * tokenization??
  * Full overview before continuing and resume programming beyond today.
7-8
* Converted 5 functions into 1 whilst reducing size by approx 150 lines.
* Using a depth counter and searching char by char is more efficient

7-10 
*Added function to differentiate polynomials
* Ran test cases including x, -x x^1 3x^-4 x^0 etc and all results ran well
*  it can easily recieve from the termsplitter function
* next will be creating differentiatiors of sin, cos, tan, ln, e, whilst managing signs and coefficients
* so d/dx -5cos = 5sin
* right now a + is added for a positive polynomial but in the end i will remove a + if it is the very first output of the final expression (after all operations)
* so that will be done in main.
* Note: a chain rule such as (-e^(3x^4 + sin(x)) will be treated as u = -e^, v = (3x^4+sin(x)). v will split terms and differentiate with sin(x) calling chain
* v' * u'(v)
* e^-() will be considered as a bad case as the negative was not distributed and simplified
* A pruning function to delete these terms will be created.
* The pruner will likely not accoutn for all cases..
* A product rule should have both the term on the left and right removed, i have decided against implementing this
* Same for quotient rule
* e^-() will be accounted. functions of coefficients will be dealt with
* a^x will be destoryed, nested inverse functions are unsimpliifed but will not be pruned I.E e^(ln(x)+x)
* Other decisions will be made
* 7-11
* Created functions to differentiate sin and cos
* setup other differentiation functions
* sin^2 will not be accepted and must be written as (sin)^2 for chain rule
* Tomorrow the rest of functions will be written (tan,ln,e) and then pruning function will begin 

7-12
* tan, ln,e differentiation finished
* Much of the code for each differentiation is exactly the same so i will create another function to offload those segments.
* organized the differentiation function to help catch unpruned functions just in case
* I saw the opportunity for it to help a little bit through some decisions and decided it was helpful this way
* I might be able to remove some code from the polynomial differentiator as a result as simple coefficients will already be removed.

  7-13/14
  *Everything is finished and recursion for chain rule is working although the result is a little crude to read but is accurate
  *7/15 will be spent optimizing and creating  a pruning function as well as testing
  *Beyond that point active development should end
  *I will try and make e^x valid instead of having to be written e^(x)
  *A menu explaining how to input will be opened from main.
