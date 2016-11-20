### Intro：

PEP8 is used for style guide for python code.

### Code layout:

Intentation: use 4 spaces per indentation level. Spaces are the preferred indentation method. Python3 disallows mixing the use of tabs and spaces for indentation. Python2 code indented with a mixtrue of tabs and spaces should be converted to using spaces exclusively. When invoking the Python2 command line interpreter with the -t option, it issues warnings about code that illegally mixes tabs and spaces. when using -tt these warnings become errors. These options are highly recommended!

### Maximum Line Length:

79 characters.

### Should a line break before or after a binary operator?

before

### Source File Encoding:

Code in the core Python distribution should always use UTF-8.

### imports:

import should usually be on separate lines:
eg:

```python
import os
import sys
from subprocess import Popen, PIPE
```
### Module level dunder names:

```python
__all__ = ['a', 'b', 'c']
__version__ = '0.1'
__author__ = 'Cardinal Biggles'
```

### String Quotes:

In Python, single quoted strings and double-quoted string are the same. For triple-quoted strings, always use double quote characters to be constistent with the docstring convention.

### Other Recommendations:

* avoid trailing whitespace anywhere. Because it's usually invisible, it can be confusing:
* always surround these binary operators with a single space oneither side: assignment, augmented assignment, comparisons, Booleans.
* if operators with different priorities are used, consider adding whitespace around the operators with the lowest priority.
* Don't use spaces around the = sign when used to indicate a keyword argument or a default parameter value.
* function annotations should use the normal rules for colons and always have spaces around the -> allow if present.
* when combining an argument annotation with a default value, use spaces around the = sign.
* Compound statements(multiple statements on the same line) are generally discouraged.
* While sometimes it's okay to put an if/for/whire with a small body on the same line, never do this for multi-clause statements. Also avoid folding such long lines.

### Naming Conventions:

The naming convention of Python's library are a bit of a mess, so we'll never get the completely consistent.

#### Overriding Principle:

Names that are visible to the use as public parts of the API should follow conventions that reflect usage rather that implementation.

#### Package and Module Names:

Modules should have short, all-lowercase names, Underscores can be used in the module name if it improves readability. 

#### Class Name:

Class names should normally use the CapWords convention.

### Programing Recommendations:

1. Code should be written in a way that does not disadvantage other implementations of Python.
2. Comparisons to singletons line None should always be done with is or is not, never the equality operators.
3. Use isnot operator rather than not ... is while both expressions are functionally identical. the former is more readable and preferred.
4. When implementing ordering operations with rich comparisons, it is best to implement all six operations rather than relying on other code only exercise a particular comparison.
5. Always use a def statement instead of an assignment statement that binds a lambda expression directly to an identifier.
6. Always use a def statement instead of an assignment statement that binds a lambda expression directly to an identifier.
7. Derive exceptions from Exception rather than BaseExption. Direct inheritance from BaseException is reserved for exceptions where catching them is almost always the wrong thing to do.
8. When raising an exception in Python 2 use raise ValueError('Message') instead of the older form raise ValueError, 'Message'.
9. Use string method instead of the string module.
10. Object type comparisons should always use isinstance() instead of comparing types directly.

### Function Annotations:





