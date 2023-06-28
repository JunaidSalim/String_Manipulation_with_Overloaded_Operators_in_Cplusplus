# String-Manipulation-with-Overloaded-Operators-in-C-
 A class that provides various string operations including concatenation, comparison, indexing, sub-string extraction, assignment, and shifting.

This repository contains a C++ program that implements a custom string class called `STRING`. The `STRING` class provides several overloaded operators and member functions for performing various operations on strings.

**Features**
- String concatenation using the `+` operator
- In-place string concatenation using the `+=` operator
- Accessing individual characters using the `[]` operator
- String equality and inequality comparison using the `==` and `!=` operators
- String comparison using the `>` and `<` operators
- Extracting sub-strings using the `()` operator
- Assignment of one string to another using the `=` operator
- Left shift and right shift operations to shift characters within the string
- Getting the size of the string

**Usage**
1. Clone the repository or download the source code files.
2. Compile the source code using a C++ compiler of your choice.
3. Run the compiled executable file.

**Code Explanation**
- The `STRING` class is defined with various member functions and overloaded operators.
- The constructor `STRING(char a[])` initializes the string with the provided character array.
- The overloaded `+` operator (`operator+`) performs string concatenation between two `STRING` objects.
- The overloaded `+=` operator (`operator+=`) performs in-place string concatenation on a `STRING` object.
- The overloaded `[]` operator (`operator[]`) allows access to individual characters of the string.
- The overloaded `==` operator (`operator==`) compares two `STRING` objects for equality.
- The overloaded `!=` operator (`operator!=`) compares two `STRING` objects for inequality.
- The overloaded `>` and `<` operators (`operator>` and `operator<`) compare two `STRING` objects.
- The overloaded `()` operator (`operator()`) extracts a sub-string from a `STRING` object.
- The overloaded `=` operator (`operator=`) assigns one `STRING` object to another.
- The overloaded `<<` and `>>` operators (`operator<<` and `operator>>`) allow input and output of `STRING` objects using stream operators.
- The `sizeofarray` and `sizeofstring` member functions are used to determine the size of character arrays and C++ strings, respectively.
- The `main` function demonstrates the usage of the `STRING` class by performing various operations on `STRING` objects.

**Contributing**
Contributions to the project are welcome. If you find any issues or have suggestions for improvements, please feel free to open an issue or submit a pull request.
