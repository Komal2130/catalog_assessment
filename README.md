# catalog_assessment

# Polynomial Constant Term Computation

## Problem Statement

This project involves computing the constant term of a polynomial using given roots and their respective base representations. The polynomial is represented as:

\[ f(x) = a_m x^m + a_{m-1} x^{m-1} + \ldots + a_1 x + c \]

Where:
- \( m \) is the degree of the polynomial.
- \( a_m, a_{m-1}, \ldots, a_1, c \) are the coefficients (real numbers).
- \( a_m \neq 0 \) (ensuring it's a polynomial of degree \( m \)).

The constant term \( c \) can be computed using the given roots of the polynomial. For this problem, you are provided with a JSON structure containing:
- Number of roots (`n`).
- Minimum number of roots required to solve for the coefficients (`k`).


### Input Format

The input is provided as a JSON string with the following structure:

```json
{
    "keys": {
        "n": <number_of_roots>,
        "k": <minimum_roots_required>
    },
    "<index>": {
        "base": "<numerical_base>",
        "value": "<value_in_base>"
    },
    ...
}
```

Where:
- `<number_of_roots>` is the total number of roots provided.
- `<minimum_roots_required>` is \( k \), the number of roots required to solve for the polynomial coefficients.
- `<index>` is a unique identifier for each root.
- `<numerical_base>` is the base in which the value is represented.
- `<value_in_base>` is the value of the root in the specified base.

### Example Input

```json
{
    "keys": {
        "n": 4,
        "k": 3
    },
    "1": {
        "base": "10",
        "value": "4"
    },
    "2": {
        "base": "2",
        "value": "111"
    },
    "3": {
        "base": "10",
        "value": "12"
    },
    "6": {
        "base": "4",
        "value": "213"
    }
}
```

### Output

The output is the constant term \( c \) of the polynomial, computed based on the provided roots.

### Setup and Execution


1. **Install Node.js**

   Ensure you have Node.js installed.

2. **Run the Code**

   Save the provided JavaScript code in a file named `Index.js`.

   ```bash
   node Index.js
   ```

3. **Expected Output**

   The script will output the constant term \( c \) to the console. For the given example, the output will be:

   ```
   The constant term c is: 3 and 28735619723864 for the two provided test case.
   ```

