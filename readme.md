#  Week3 Advanced Calculator 

**This advanced Calculator does the below functions**:
1. Add, Subtract, Multiply, and Divide
2. Throw exception for divide by zero and test that the exception is thrown
3. This will store history of calculations, so that we can retrieve the last calculation, add a calculation, 
4. This code has 100% test coverage, passing pylint and 100% pytest coverage.  
5. Implemented a pytest fixture to test  

**set up:**
Python Virtual Environments: Essential for managing project-specific dependencies.
Pytest: A powerful framework for writing and running Python tests.
Pylint: A tool for analyzing your Python code for errors and enforcing a coding standard.
Coverage: A tool for measuring the coverage of your unit tests.

Main Principes followed:
1) Follow DRY Principle (Don't Repeat Yourself)
2) Separation of Concerns -- Separate each part that the program needs to do, so it is organized and the functionals only have to do ONE thing.

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
