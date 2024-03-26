# generator functions-3

Using generator functions to parse and process files line by line in Python is a memory-efficient approach, especially for large files. Here's an example of how you can achieve this:

```python
def process_file(filename):
    with open(filename, 'r') as file:
        for line in file:
            # Process each line here
            yield line.strip()  # Example: yield stripped line

# Example usage
filename = 'example.txt'
for line in process_file(filename):
    # Process each line further if needed
    print(line)
```

In this example:

1. We define a generator function `process_file` that takes a filename as input.
2. Inside the function, we open the file using `with open(filename, 'r') as file:` which ensures that the file is properly closed after its suite finishes, even if an exception is raised.
3. We iterate through each line in the file using a `for` loop.
4. Within the loop, we process each line as needed. In this example, we're simply yielding the stripped version of each line, but you can perform more complex processing as required.
5. The `yield` statement returns the processed line to the caller without terminating the function's execution. This allows the function to resume from where it left off the next time it's called.
6. When the loop finishes, the function ends, and the file is closed automatically due to the `with` statement.
7. We can then iterate over the generator returned by `process_file`, processing each line further or performing any required operations.

This approach allows you to efficiently process files of any size without loading the entire file into memory at once.
