
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
