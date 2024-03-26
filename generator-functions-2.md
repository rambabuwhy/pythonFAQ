# Generator functions-2

1. **What is the difference between a generator function and a normal function in Python?**
   * A generator function contains one or more `yield` statements and returns a generator iterator when called. It generates a series of values lazily on-the-fly, while a normal function executes all its statements and returns a single value.
2. **Explain the concept of lazy evaluation and how it relates to generators.**
   * Lazy evaluation means delaying the evaluation of an expression until its value is actually needed. Generators implement lazy evaluation by generating values only when requested, which conserves memory and allows processing of large datasets efficiently.
3. **How can you iterate over the values produced by a generator?**
   * You can iterate over the values produced by a generator using a `for` loop or by calling the `next()` function on the generator object until a `StopIteration` exception is raised.
4. **What happens when a generator function is called?**
   * When a generator function is called, it returns a generator iterator without executing the function's body. The function's execution starts only when the `next()` function is called on the generator iterator.
5. **Can you use a generator inside a list comprehension? If so, how?**
   * Yes, you can use a generator expression inside a list comprehension by enclosing the generator expression in square brackets. For example: `[x for x in range(10) if x % 2 == 0]`.
6. **How do you create an infinite generator in Python?**
   * You can create an infinite generator by using a `while` loop inside a generator function and yielding values indefinitely.
7. **What is the purpose of the `yield from` statement in Python?**
   * The `yield from` statement delegates the execution of a sub-generator to the current generator. It simplifies the implementation of generators that yield values from nested generators.
8. **Explain the term "generator expression" in Python.**
   * A generator expression is a concise way to create a generator. It has a syntax similar to list comprehensions but uses parentheses instead of square brackets.
9. **What are the advantages of using generators over lists in Python?**
   * Generators are memory efficient as they produce values lazily, reducing memory consumption.
   * They can represent infinite sequences.
   * They allow for simpler and more readable code, especially when dealing with large datasets or streams of data.
10. **Can you modify the state of a generator from outside? Why or why not?**
    * No, you cannot modify the state of a generator from outside because generators encapsulate their state internally, and there's no direct way to access or modify this state from outside the generator.
11. **How can you pass arguments to a generator function?**
    * You can pass arguments to a generator function by providing them as parameters when calling the function.
12. **What happens if you call `return` instead of `yield` in a generator function?**
    * If you call `return` in a generator function, it raises a `StopIteration` exception, indicating that the generator has exhausted its iteration and has no more values to yield.
13. **Explain the concept of generator chaining.**
    * Generator chaining involves combining multiple generators to produce a single generator that yields values from all the constituent generators sequentially.
14. **What are some common use cases for generators in Python?**
    * Generating an infinite sequence of values.
    * Processing large datasets lazily.
    * Implementing pipeline processing of data.
    * Efficiently parsing and processing files line by line.
15. **How does the memory consumption of generators compare to that of lists?**
    * Generators typically consume less memory than lists because they produce values lazily and do not store all values in memory at once, unlike lists which store all values in memory simultaneously. This makes generators more memory efficient, especially when dealing with large datasets.
