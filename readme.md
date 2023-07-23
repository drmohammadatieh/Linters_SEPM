## Introduction

This is an exercise on using linters to achieve Python code quality as part of the Software Engineering Project Management course the CS PgDip at the University of Essex Online. 

Now run the code against a variety of linters to test the code quality:

pylint code_with_lint.py
pyflakes code_with_lint.py
pycodestyle code_with_lint.py
pydocstyle code_with_lint.py
Compare the effectiveness of each tool in defining and identifying code quality.

## Pylint

*Output:*

************* Module code_with_lint
code_with_lint.py:29:0: W0301: Unnecessary semicolon (unnecessary-semicolon)
code_with_lint.py:33:0: C0325: Unnecessary parens after 'return' keyword (superfluous-parens)
code_with_lint.py:35:0: C0325: Unnecessary parens after 'return' keyword (superfluous-parens)
code_with_lint.py:46:0: C0304: Final newline missing (missing-final-newline)
code_with_lint.py:1:0: C0114: Missing module docstring (missing-module-docstring)
code_with_lint.py:4:0: W0622: Redefining built-in 'pow' (redefined-builtin)
code_with_lint.py:4:0: W0401: Wildcard import math (wildcard-import)
code_with_lint.py:9:0: C0103: Constant name "some_global_var" doesn't conform to UPPER_CASE naming style (invalid-name)
code_with_lint.py:11:13: C0103: Argument name "x" doesn't conform to snake_case naming style (invalid-name)
code_with_lint.py:11:16: C0103: Argument name "y" doesn't conform to snake_case naming style (invalid-name)
code_with_lint.py:15:4: W0621: Redefining name 'some_global_var' from outer scope (line 9) (redefined-outer-name)
code_with_lint.py:18:4: W0101: Unreachable code (unreachable)
code_with_lint.py:15:4: W0612: Unused variable 'some_global_var' (unused-variable)
code_with_lint.py:21:17: C0103: Argument name "x" doesn't conform to snake_case naming style (invalid-name)
code_with_lint.py:21:20: C0103: Argument name "y" doesn't conform to snake_case naming style (invalid-name)
code_with_lint.py:27:7: C0121: Comparison 'x != None' should be 'x is not None' (singleton-comparison)
code_with_lint.py:30:12: R1705: Unnecessary "else" after "return", remove the "else" and de-indent the code inside it (no-else-return)
code_with_lint.py:21:0: R1710: Either all return statements in a function should return an expression, or none of them should. (inconsistent-return-statements)
code_with_lint.py:37:0: C0115: Missing class docstring (missing-class-docstring)
code_with_lint.py:43:8: W0621: Redefining name 'time' from outer scope (line 7) (redefined-outer-name)
code_with_lint.py:43:15: E0601: Using variable 'time' before assignment (used-before-assignment)
code_with_lint.py:44:8: C0415: Import outside toplevel (datetime.datetime) (import-outside-toplevel)
code_with_lint.py:39:4: R1711: Useless return at end of function or method (useless-return)
code_with_lint.py:39:50: W0613: Unused argument 'verbose' (unused-argument)
code_with_lint.py:42:8: W0612: Unused variable 'list_comprehension' (unused-variable)
code_with_lint.py:45:8: W0612: Unused variable 'date_and_time' (unused-variable)
code_with_lint.py:37:0: R0903: Too few public methods (0/2) (too-few-public-methods)
code_with_lint.py:3:0: W0611: Unused import io (unused-import)
code_with_lint.py:7:0: W0611: Unused time imported from time (unused-import)
code_with_lint.py:4:0: W0614: Unused import(s) acos, acosh, asin, asinh, atan, atan2, atanh, cbrt, ceil, comb, copysign, cos, cosh, degrees, dist, e, erf, erfc, exp, exp2, expm1, fabs, factorial, floor, fmod, frexp, fsum, gamma, gcd, hypot, inf, isclose, isfinite, isinf, isnan, isqrt, lcm, ldexp, lgamma, log, log10, log1p, log2, modf, nan, nextafter, perm, pow, prod, radians, remainder, sin, sinh, sqrt, tan, tanh, tau, trunc and ulp from wildcard import of math (unused-wildcard-import)

------------------------------------------------------------------
Your code has been rated at 0.00/10 (previous run: 0.00/10, +0.00)


## Pyflakes

*Output*:

code_with_lint.py:3:1: 'io' imported but unused
code_with_lint.py:4:1: 'from math import *' used; unable to detect undefined names
code_with_lint.py:15:5: local variable 'some_global_var' is assigned to but never used
code_with_lint.py:42:44: 'pi' may be undefined, or defined from star imports: math
code_with_lint.py:42:9: local variable 'list_comprehension' is assigned to but never used
code_with_lint.py:43:16: local variable 'time' defined in enclosing scope on line 7 referenced before assignment
code_with_lint.py:43:9: local variable 'time' is assigned to but never used
code_with_lint.py:45:9: local variable 'date_and_time' is assigned to but never used


## Pycodestyle

*Output*:

code_with_lint.py:11:1: E302 expected 2 blank lines, found 1
code_with_lint.py:16:15: E225 missing whitespace around operator
code_with_lint.py:21:1: E302 expected 2 blank lines, found 1
code_with_lint.py:22:80: E501 line too long (80 > 79 characters)
code_with_lint.py:27:10: E711 comparison to None should be 'if cond is not None:'
code_with_lint.py:29:25: E703 statement ends with a semicolon
code_with_lint.py:33:23: E275 missing whitespace after keyword
code_with_lint.py:33:24: E201 whitespace after '('
code_with_lint.py:37:1: E302 expected 2 blank lines, found 1
code_with_lint.py:39:58: E251 unexpected spaces around keyword / parameter equals
code_with_lint.py:39:60: E251 unexpected spaces around keyword / parameter equals
code_with_lint.py:40:28: E221 multiple spaces before operator
code_with_lint.py:40:31: E222 multiple spaces after operator
code_with_lint.py:41:22: E221 multiple spaces before operator
code_with_lint.py:41:31: E222 multiple spaces after operator
code_with_lint.py:42:80: E501 line too long (83 > 79 characters)
code_with_lint.py:46:15: W292 no newline at end of file


## Pydocstyle

*Output*:

code_with_lint.py:1 at module level:
        D100: Missing docstring in public module
code_with_lint.py:12 in public function `multiply`:
        D200: One-line docstring should fit on one line with quotes (found 3)
code_with_lint.py:12 in public function `multiply`:
        D400: First line should end with a period (not 's')
code_with_lint.py:12 in public function `multiply`:
        D401: First line should be in imperative mood; try rephrasing (found 'This')
code_with_lint.py:22 in public function `is_sum_lucky`:
        D205: 1 blank line required between summary line and description (found 0)
code_with_lint.py:22 in public function `is_sum_lucky`:
        D400: First line should end with a period (not 'y')
code_with_lint.py:22 in public function `is_sum_lucky`:
        D401: First line should be in imperative mood; try rephrasing (found 'This')
code_with_lint.py:37 in public class `SomeClass`:
        D101: Missing docstring in public class
code_with_lint.py:39 in public method `__init__`:
        D107: Missing docstring in __init__
Mohammad@MacBook-Pro Linters % pydocstyle code_with_lint.py
code_with_lint.py:1 at module level:
        D100: Missing docstring in public module
code_with_lint.py:11 in public function `multiply`:
        D200: One-line docstring should fit on one line with quotes (found 3)
code_with_lint.py:11 in public function `multiply`:
        D400: First line should end with a period (not 's')
code_with_lint.py:11 in public function `multiply`:
        D401: First line should be in imperative mood; try rephrasing (found 'This')
code_with_lint.py:21 in public function `is_sum_lucky`:
        D205: 1 blank line required between summary line and description (found 0)
code_with_lint.py:21 in public function `is_sum_lucky`:
        D400: First line should end with a period (not 'y')
code_with_lint.py:21 in public function `is_sum_lucky`:
        D401: First line should be in imperative mood; try rephrasing (found 'This')
code_with_lint.py:36 in public class `SomeClass`:
        D101: Missing docstring in public class
code_with_lint.py:38 in public method `__init__`:
        D107: Missing docstring in __init__



## Question

Compare the effectiveness of each tool in defining and identifying code quality. What can you conclude about the effectiveness of each approach?

*Answer*:

Each one of the tools has its uses with some overlap between them. The most extensive one is Pylint.

- Pylint is an extensive static code analyzer that detects code errors like unused variables and unreachable code; and coding style problems (Anon,n.d).

-Pyflakes is less extensive and it seems it focuses on coding errors, but not styles.

-Pycodestyle is used to check for errors in coding style only.

-Pydocstyle is used to check for errors in documentation style only.


## References

Anon (n.d.). Pylint 2.17.4 documentation. Available from: https://pylint.readthedocs.io/en/stable/ [Accessed 23 Jul. 2023].

‌



