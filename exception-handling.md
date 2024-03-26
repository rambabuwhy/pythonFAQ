# exception handling

In Python, `try`, `except`, `else`, and `finally` are keywords used for exception handling. Here's a brief explanation of each:

1. **`try`**: It is used to wrap the code that might raise an exception.
2. **`except`**: It catches the exceptions that occur within the `try` block. You can specify which exceptions you want to catch or catch all exceptions using a generic `except` clause.
3. **`else`**: This block is executed if the code inside the `try` block doesn't raise any exceptions.
4. **`finally`**: This block is always executed regardless of whether an exception occurred or not. It is typically used for cleanup actions, such as closing files or releasing resources.

Here's a basic example to illustrate the usage:

```python
try:
    # Code that might raise an exception
    x = int(input("Enter a number: "))
    result = 10 / x
except ValueError:
    print("Please enter a valid number.")
except ZeroDivisionError:
    print("Cannot divide by zero.")
else:
    print("Division was successful.")
finally:
    print("This will always execute, regardless of exceptions.")
```

In this example:

* If the user enters a non-numeric value, a `ValueError` will be raised.
* If the user enters zero, a `ZeroDivisionError` will be raised.
* If the user enters a valid number other than zero, the division operation will succeed.
* In any case, the `finally` block will execute to perform cleanup tasks.

Remember, the `else` block will execute only if no exceptions occur in the `try` block. If an exception occurs, the `else` block will be skipped. The `finally` block always executes, whether an exception occurred or not.
