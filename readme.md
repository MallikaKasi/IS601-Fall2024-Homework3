#  Week3 Advanced Calculator that does below functions

## Notes on Advanced Calculator
The advanced calculator in part 3 contains static methods on the Calculator, instance methods on the Calculation, and class methods on the Calculations class.  In addition, it has more advanced testing that uses parameterized test data and a fixture to make it easy to setup each test with consistent data.  There are also modifciations to the .pylintrc file to control pylint's code analysis and I disable pylint errors in the calculator/calculation.py file by putting this code at the top of the file, which you can also use inside a specific function to disable a pylint check for a specific file.   You sometimes need to disable pylint when you know you are doing the correct thing, but that for some reason pylint doesn't understand.  It's better to disable it at the function or file level than the global level because you never know when you really do want it to tell you the style error.

**This Calculator does the below functions**:
1. Add, Subtract, Multiply, and Divide
2. Throw exception for divide by zero and test that the exception is thrown
3. Use at least one class, at least one static method, at least one class method.
4. It needs to  store a history of calculations, so that you can retrieve the last calculation, add a calculation, 
5. It needs to have 100% test coverage, pass pylint, and you need to do your best to not repeat any lines of code.  
6.  You should use type hints for input parameter types and return types.
7.  Implement a pytest fixture to test the 

### Test Results
(venv) mallikakasi@HOME:~/NJIT-FALL-2024/IS601-Projects/Week3/Week3_Project$ pytest
======================================================================== test session starts =========================================================================
platform linux -- Python 3.10.12, pytest-8.0.0, pluggy-1.4.0 -- /home/mallikakasi/NJIT-FALL-2024/IS601-Projects/Week2/Week2_Project/venv/bin/python
cachedir: .pytest_cache
rootdir: /home/mallikakasi/NJIT-FALL-2024/IS601-Projects/Week3/Week3_Project
configfile: pytest.ini
testpaths: tests
plugins: pylint-0.21.0, cov-4.1.0
collected 25 items                                                                                                                                                   

tests/test_calculation.py::test_calculation_operations[a0-b0-add-expected0] PASSED                                                                             [  4%]
tests/test_calculation.py::test_calculation_operations[a1-b1-subtract-expected1] PASSED                                                                        [  8%]
tests/test_calculation.py::test_calculation_operations[a2-b2-multiply-expected2] PASSED                                                                        [ 12%]
tests/test_calculation.py::test_calculation_operations[a3-b3-divide-expected3] PASSED                                                                          [ 16%]
tests/test_calculation.py::test_calculation_operations[a4-b4-add-expected4] PASSED                                                                             [ 20%]
tests/test_calculation.py::test_calculation_operations[a5-b5-subtract-expected5] PASSED                                                                        [ 24%]
tests/test_calculation.py::test_calculation_operations[a6-b6-multiply-expected6] PASSED                                                                        [ 28%]
tests/test_calculation.py::test_calculation_operations[a7-b7-divide-expected7] PASSED                                                                          [ 32%]
tests/test_calculation.py::test_calculation_repr PASSED                                                                                                        [ 36%]
tests/test_calculation.py::test_divide_by_zero PASSED                                                                                                          [ 40%]
tests/test_calculations.py::test_add_calculation PASSED                                                                                                        [ 44%]
tests/test_calculations.py::test_get_history PASSED                                                                                                            [ 48%]
tests/test_calculations.py::test_clear_history PASSED                                                                                                          [ 52%]
tests/test_calculations.py::test_get_latest PASSED                                                                                                             [ 56%]
tests/test_calculations.py::test_find_by_operation PASSED                                                                                                      [ 60%]
tests/test_calculations.py::test_get_latest_with_empty_history PASSED                                                                                          [ 64%]
tests/test_calculator.py::test_addition PASSED                                                                                                                 [ 68%]
tests/test_calculator.py::test_subtraction PASSED                                                                                                              [ 72%]
tests/test_calculator.py::test_multiply PASSED                                                                                                                 [ 76%]
tests/test_calculator.py::test_divide PASSED                                                                                                                   [ 80%]
tests/test_operations.py::test_operation_add PASSED                                                                                                            [ 84%]
tests/test_operations.py::test_operation_subtract PASSED                                                                                                       [ 88%]
tests/test_operations.py::test_operation_multiply PASSED                                                                                                       [ 92%]
tests/test_operations.py::test_operation_divide PASSED                                                                                                         [ 96%]
tests/test_operations.py::test_divide_by_zero PASSED                                                                                                           [100%]

========================================================================= 25 passed in 0.05s =========================================================================
(venv) mallikakasi@HOME:~/NJIT-FALL-2024/IS601-Projects/Week3/Week3_Project$ pytest --pylint 
======================================================================== test session starts =========================================================================
platform linux -- Python 3.10.12, pytest-8.0.0, pluggy-1.4.0 -- /home/mallikakasi/NJIT-FALL-2024/IS601-Projects/Week2/Week2_Project/venv/bin/python
cachedir: .pytest_cache
rootdir: /home/mallikakasi/NJIT-FALL-2024/IS601-Projects/Week3/Week3_Project
configfile: pytest.ini
testpaths: tests
plugins: pylint-0.21.0, cov-4.1.0
collected 30 items                                                                                                                                                   

tests/__init__.py::PYLINT SKIPPED (file(s) previously passed pylint checks)                                                                                    [  3%]
tests/test_calculation.py::PYLINT SKIPPED (file(s) previously passed pylint checks)                                                                            [  6%]
tests/test_calculation.py::test_calculation_operations[a0-b0-add-expected0] PASSED                                                                             [ 10%]
tests/test_calculation.py::test_calculation_operations[a1-b1-subtract-expected1] PASSED                                                                        [ 13%]
tests/test_calculation.py::test_calculation_operations[a2-b2-multiply-expected2] PASSED                                                                        [ 16%]
tests/test_calculation.py::test_calculation_operations[a3-b3-divide-expected3] PASSED                                                                          [ 20%]
tests/test_calculation.py::test_calculation_operations[a4-b4-add-expected4] PASSED                                                                             [ 23%]
tests/test_calculation.py::test_calculation_operations[a5-b5-subtract-expected5] PASSED                                                                        [ 26%]
tests/test_calculation.py::test_calculation_operations[a6-b6-multiply-expected6] PASSED                                                                        [ 30%]
tests/test_calculation.py::test_calculation_operations[a7-b7-divide-expected7] PASSED                                                                          [ 33%]
tests/test_calculation.py::test_calculation_repr PASSED                                                                                                        [ 36%]
tests/test_calculation.py::test_divide_by_zero PASSED                                                                                                          [ 40%]
tests/test_calculations.py::PYLINT SKIPPED (file(s) previously passed pylint checks)                                                                           [ 43%]
tests/test_calculations.py::test_add_calculation PASSED                                                                                                        [ 46%]
tests/test_calculations.py::test_get_history PASSED                                                                                                            [ 50%]
tests/test_calculations.py::test_clear_history PASSED                                                                                                          [ 53%]
tests/test_calculations.py::test_get_latest PASSED                                                                                                             [ 56%]
tests/test_calculations.py::test_find_by_operation PASSED                                                                                                      [ 60%]
tests/test_calculations.py::test_get_latest_with_empty_history PASSED                                                                                          [ 63%]
tests/test_calculator.py::PYLINT SKIPPED (file(s) previously passed pylint checks)                                                                             [ 66%]
tests/test_calculator.py::test_addition PASSED                                                                                                                 [ 70%]
tests/test_calculator.py::test_subtraction PASSED                                                                                                              [ 73%]
tests/test_calculator.py::test_multiply PASSED                                                                                                                 [ 76%]
tests/test_calculator.py::test_divide PASSED                                                                                                                   [ 80%]
tests/test_operations.py::PYLINT SKIPPED (file(s) previously passed pylint checks)                                                                             [ 83%]
tests/test_operations.py::test_operation_add PASSED                                                                                                            [ 86%]
tests/test_operations.py::test_operation_subtract PASSED                                                                                                       [ 90%]
tests/test_operations.py::test_operation_multiply PASSED                                                                                                       [ 93%]
tests/test_operations.py::test_operation_divide PASSED                                                                                                         [ 96%]
tests/test_operations.py::test_divide_by_zero PASSED                                                                                                           [100%]

=================================================================== 25 passed, 5 skipped in 0.11s ====================================================================
(venv) mallikakasi@HOME:~/NJIT-FALL-2024/IS601-Projects/Week3/Week3_Project$ pytest --pylint --cov
======================================================================== test session starts =========================================================================
platform linux -- Python 3.10.12, pytest-8.0.0, pluggy-1.4.0 -- /home/mallikakasi/NJIT-FALL-2024/IS601-Projects/Week2/Week2_Project/venv/bin/python
cachedir: .pytest_cache
rootdir: /home/mallikakasi/NJIT-FALL-2024/IS601-Projects/Week3/Week3_Project
configfile: pytest.ini
testpaths: tests
plugins: pylint-0.21.0, cov-4.1.0
collected 30 items                                                                                                                                                   

tests/__init__.py::PYLINT SKIPPED (file(s) previously passed pylint checks)                                                                                    [  3%]
tests/test_calculation.py::PYLINT SKIPPED (file(s) previously passed pylint checks)                                                                            [  6%]
tests/test_calculation.py::test_calculation_operations[a0-b0-add-expected0] PASSED                                                                             [ 10%]
tests/test_calculation.py::test_calculation_operations[a1-b1-subtract-expected1] PASSED                                                                        [ 13%]
tests/test_calculation.py::test_calculation_operations[a2-b2-multiply-expected2] PASSED                                                                        [ 16%]
tests/test_calculation.py::test_calculation_operations[a3-b3-divide-expected3] PASSED                                                                          [ 20%]
tests/test_calculation.py::test_calculation_operations[a4-b4-add-expected4] PASSED                                                                             [ 23%]
tests/test_calculation.py::test_calculation_operations[a5-b5-subtract-expected5] PASSED                                                                        [ 26%]
tests/test_calculation.py::test_calculation_operations[a6-b6-multiply-expected6] PASSED                                                                        [ 30%]
tests/test_calculation.py::test_calculation_operations[a7-b7-divide-expected7] PASSED                                                                          [ 33%]
tests/test_calculation.py::test_calculation_repr PASSED                                                                                                        [ 36%]
tests/test_calculation.py::test_divide_by_zero PASSED                                                                                                          [ 40%]
tests/test_calculations.py::PYLINT SKIPPED (file(s) previously passed pylint checks)                                                                           [ 43%]
tests/test_calculations.py::test_add_calculation PASSED                                                                                                        [ 46%]
tests/test_calculations.py::test_get_history PASSED                                                                                                            [ 50%]
tests/test_calculations.py::test_clear_history PASSED                                                                                                          [ 53%]
tests/test_calculations.py::test_get_latest PASSED                                                                                                             [ 56%]
tests/test_calculations.py::test_find_by_operation PASSED                                                                                                      [ 60%]
tests/test_calculations.py::test_get_latest_with_empty_history PASSED                                                                                          [ 63%]
tests/test_calculator.py::PYLINT SKIPPED (file(s) previously passed pylint checks)                                                                             [ 66%]
tests/test_calculator.py::test_addition PASSED                                                                                                                 [ 70%]
tests/test_calculator.py::test_subtraction PASSED                                                                                                              [ 73%]
tests/test_calculator.py::test_multiply PASSED                                                                                                                 [ 76%]
tests/test_calculator.py::test_divide PASSED                                                                                                                   [ 80%]
tests/test_operations.py::PYLINT SKIPPED (file(s) previously passed pylint checks)                                                                             [ 83%]
tests/test_operations.py::test_operation_add PASSED                                                                                                            [ 86%]
tests/test_operations.py::test_operation_subtract PASSED                                                                                                       [ 90%]
tests/test_operations.py::test_operation_multiply PASSED                                                                                                       [ 93%]
tests/test_operations.py::test_operation_divide PASSED                                                                                                         [ 96%]
tests/test_operations.py::test_divide_by_zero PASSED                                                                                                           [100%]

---------- coverage: platform linux, python 3.10.12-final-0 ----------
Name                         Stmts   Miss  Cover
------------------------------------------------
calculator/__init__.py          22      0   100%
calculator/calculation.py       15      0   100%
calculator/calculations.py      22      0   100%
calculator/operations.py        11      0   100%
tests/__init__.py                0      0   100%
tests/test_calculation.py       16      0   100%
tests/test_calculations.py      31      0   100%
tests/test_calculator.py         9      0   100%
tests/test_operations.py        20      0   100%
------------------------------------------------
TOTAL                          146      0   100%


=================================================================== 25 passed, 5 skipped in 0.27s ====================================================================
(venv) mallikakasi@HOME:~/NJIT-FALL-2024/IS601-Projects/Week3/Week3_Project$ 
