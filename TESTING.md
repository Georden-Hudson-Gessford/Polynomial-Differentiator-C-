


* Version #4

* Test:                        Pass?             Output:
* 85x^2+4x^-2+4x^3+4+x+5     |  Yes.             | 10x^1 -8x^-3 +12x^2  +1 
* 8x+x+x+x+x                 |  Yes.             | 1  +1 +1 +1 +1 


* Version #5

* Polydiff.cpp
* "x"  {Pass}
* "-x" {Pass}
* "7" {Pass}
* "0" {Pass}
* "x^0" {Pass}
* "x^1" {Pass}
* "-7x" {Pass}
* "-3x^10" {Pass}
* "5x^1" {Pass}
* ---------------
* Complete program tests
* Chain rule will give unexpanded expressions, the sign between expressions will be lost until expanded
* "sin(x)" Expected result = (1*cos(x)) {Pass}
* "e^(x)" Expected result = (1*e^(x))" {Pass}
* "tan(x)" Expected result = (1*sec^2(x)) {Pass}
*  "cos(x)" Expected result = (1*-sin(x)) [Pass}
* "ln(x)" Expected result = (1*1/(x)) {Pass}
* "5x^3" Expected  result = "15x^2" {Pass}
*  "-5x^-4" Expected result = "+20x^-5" {Pass}
*  "400000x" Expected result = "400000" {Pass}
*  "-50000000" Expected result = ""; {Pass}
*  "-cos(5x)" Expected result = "(5*sin(5x))" {Pass}
*  "sin((ln(-x))^2)" Expected result "(((-1*1/(-x))*2ln(-x))^1))cos((ln(-x))^2)" {Pass}
*  "sin(sin(sin(sin(x))))" Expected result =
*   " ((((1*cos(x))*cos(sin(x)))*cos(sin(sin(x))))*cos(sin(sin(sin(x))))) " {Pass}
*  "5x^2 + tan(x) + tan(-x) + cos(5x^4+3)+-e^-x" Expected Result = "+10x^1 (1*+sec^2(x)) (-1*+sec^2(-x)) (+20x^3 *-sin(5x^4+3))" {Pass}
*  "5x^2 +4x^3 + 20" Expected result = "10x^1 +12x^2" {Pass}
