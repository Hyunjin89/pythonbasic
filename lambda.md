# pythonbasic #lambda

`lambda` is a keyword in Python used to create anonymous functions, also known as lambda functions. These functions are small, one-line functions that don't have a name and are typically used for simple operations. Lambda functions are particularly useful when you need a short, throwaway function for a specific task. The syntax for a lambda function is as follows:

```python
lambda arguments: expression
```

Here's how to use `lambda` functions:

1. **Basic Usage**:
   
   ```python
   # Define a lambda function that adds two numbers
   add = lambda x, y: x + y

   # Use the lambda function
   result = add(3, 5)  # result will be 8
   ```

   In this example, we define a lambda function `add` that takes two arguments and returns their sum.

2. **As a Function Argument**:

   Lambda functions are often used as arguments to higher-order functions like `map`, `filter`, and `sorted`. For example:

   ```python
   numbers = [1, 5, 3, 9, 2, 6]

   # Use a lambda function with map to square each number
   squared = list(map(lambda x: x**2, numbers))

   # Use a lambda function with filter to get even numbers
   even_numbers = list(filter(lambda x: x % 2 == 0, numbers))

   # Use a lambda function with sorted to sort a list of tuples by the second element
   data = [(2, 3), (1, 5), (4, 2)]
   sorted_data = sorted(data, key=lambda x: x[1])
   ```

   In these examples, lambda functions are used to define custom behavior for the `map`, `filter`, and `sorted` functions.

3. **Using with Key Functions**:

   Lambda functions are also commonly used with functions like `max` and `min` to specify a custom key for finding the maximum or minimum value in a list:

   ```python
   students = [
       {'name': 'Alice', 'grade': 95},
       {'name': 'Bob', 'grade': 88},
       {'name': 'Charlie', 'grade': 92}
   ]

   # Find the student with the highest grade using a lambda function as the key
   top_student = max(students, key=lambda student: student['grade'])
   ```

   In this example, the lambda function is used as the key to find the student with the highest grade.

Lambda functions are simple and handy for short, straightforward operations. However, for more complex functions, it's often better to define a regular named function using `def` for clarity and reusability.
