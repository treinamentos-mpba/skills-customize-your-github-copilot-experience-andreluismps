# 📘 Assignment: Testing Python Functions with pytest

## 🎯 Objective

Write and run automated tests for Python functions using `pytest`. Practice checking expected results, boundary cases, and invalid input so that failures help identify bugs.

## 📝 Tasks

### 🛠️ Write and Run Your First Tests

#### Description
Create `sales.py` with a `calculate_total(prices)` function that returns the sum of a list of prices. Create `test_sales.py` and use `pytest` to check the function.

#### Requirements
The completed program must:

- Return the sum of all prices in the list.
- Return `0` for an empty list.
- Include at least three tests in `test_sales.py`, including a normal list, a single price, and an empty list.
- Run the tests with `python -m pytest`.

### 🛠️ Test Discounts and Invalid Inputs

#### Description
Add an `apply_discount(total, percentage)` function to `sales.py`. Write tests for ordinary discounts, boundary values, and invalid inputs.

#### Requirements
The completed program must:

- Subtract the given percentage from a non-negative total.
- Accept percentages from `0` through `100`, inclusive.
- Raise `ValueError` if the total is negative or the percentage is outside that range.
- Include tests for a regular discount, `0%`, `100%`, and invalid values, using `pytest.raises` to check exceptions.

### 🛠️ Run and Review the Full Test Suite

#### Description
Run all tests together and add one test for a case that is not already covered. Use the test output to correct any behavior that does not match the requirements.

#### Requirements
The completed program must:

- Pass all tests when run with `python -m pytest -q`.
- Include at least one additional test for a meaningful input or boundary case.
- Keep the tests in `test_sales.py` and name test functions with the `test_` prefix so pytest can discover them.
