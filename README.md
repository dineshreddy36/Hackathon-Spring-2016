# Expression Parser
This repository is for Hackathon competition project which is of building Algorithm to solve the expression. Below is the usecase.

                           ERICSSON USE CASE 1

Given a string representing an expression which consists of non-negative round numbers and four basic arithmetic operations, 
write a function which calculates final value of the expression. 
Although only non-negative numbers are allowed, end result or intermediate results may be negative. 
Four operations are: +, -, * and / . Expression may contain parentheses. 
Assume that expression is syntactically correct: all operators have proper left and right operand, parentheses are properly nested 
and balanced.

Examples:

	(3+2) <= 5 produces result true. 4/3 > 1 produces result true. 

	(3+6/2)/4 == 3 produces true. 

	(A1/A1_avg)100 > 90 produces true given A1= 95 and A1_avg = 90. 

	(A1/A1_avg)100 <= 90 && (A1/A1_avg)100 > 80 produces true given A1= 85 and A1_avg = 90


Code should accept list to input variables and the list of expressions and return the list of outputs.

IMPLEMENTATION :

 This is basically an algorithm for evaluating the string of expression or the list of mathematical expressions. The input to the algorithm can be two files, one having all expressions and other having list of variables, the output will also be a file listing expression and results side by side. Results could be true or false. 
 
The algorithm is divided in three parts:

1.	First part takes strings in one list and other list for variables. Then it will replace all variables in the strings with respective values. As this program works for list of inputs and so it evaluates them one by one.
Next two steps are of processing individual substring one by one. When it starts processing strings one by one it does so in two steps. First part evaluates the math expression and second logical operators. 

2.	It scans string from left to right and segregating it with the logical operator ‘&&’ and ‘OR’. It takes all segregated substrings one by one and passes them to math processing method which will process them and give the result. 
Before doing the math operation, it balances the substring by removing the extra parenthesis and getting the balanced substring. The result return by the math processing method will be replaced to the original string in-place of substring.
This same process continues for all the bisected substrings and at the end it will have the string contains 1(s) and 0(s) with logical operators which it will pass to the logical processing method.

3.	The logical processing method will process this and give the result in form of true or false, final result.

The output along with original input string will be stored to output file.

![alt tag](https://github.com/hirenshah7390/Hackathon_Spring2016/blob/master/src/PerformanceGraph.png)









  
