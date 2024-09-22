#  Week3 Advanced Calculator that does below functions


## Notes on Advanced Calculator
The advanced calculator in part 3 contains static methods on the Calculator, instance methods on the Calculation, and class methods on the Calculations class.  In addition, it has more advanced testing that uses parameterized test data and a fixture to make it easy to setup each test with consistent data.  There are also modifciations to the .pylintrc file to control pylint's code analysis and I disable pylint errors in the calculator/calculation.py file by putting this code at the top of the file, which you can also use inside a specific function to disable a pylint check for a specific file.   You sometimes need to disable pylint when you know you are doing the correct thing, but that for some reason pylint doesn't understand.  It's better to disable it at the function or file level than the global level because you never know when you really do want it to tell you the style error.


1. Add, Subtract, Multiply, and Divide
2. Throw exception for divide by zero and test that the exception is thrown
3. Use at least one class, at least one static method, at least one class method.
4. It needs to  store a history of calculations, so that you can retrieve the last calculation, add a calculation, 
5. It needs to have 100% test coverage, pass pylint, and you need to do your best to not repeat any lines of code.  
6.  You should use type hints for input parameter types and return types.
7.  Implement a pytest fixture to test the 

## Grading:

1.  20  Points for (add subtract, multiply, divide) 
2.  10 Points for exception throwing and testing on divide by zero
3.  30 points each for using static, class, and instance methods correctly
4.  5 Points for having a calculation class that stores the arthitmentic operation in a instance property.
5.  15 Points for having a calculation history to store calculation instances
6.  10 Points for having the convenience methods on the calculations class to manage the history
7.  10 Points for using parameterized test data
