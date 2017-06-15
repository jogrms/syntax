# syntax
A programming language syntax proposal

## Desired Properties
### 1. Expressive
The language should be easily extendable. Adding a new programming construct should be a matter of writing a new module in the language itself, as opposed to modifying the compiler and adding a new syntax primitive. All popular modern language constructs should be easily expressible using the proposed syntax.
### 2. Lightweight
The number of language constructs the programmer has to remember should be as small as possible. In terms of grammar definition this means that there shouldn't be too many kinds of terminal symbols. Grammar definition itself should be as simple as possible
### 3. Readable
One of the best syntaxes out there is Lisp: it's very flexible and satisfies almost all the requirements of this proposal. One of the issues with lisp is that a lot of people find it hard to read, or at least it requires a great deal of getting used to. In particular, it's easier for humans to read vertical lists and have whitespace as a natural way to add structure to the text. Lisp constructs, on the other hand, are usually S-expressions that span several lines of code and require mentally keeping track of open and closed parentheses when reading.
### 4. Suitable for version control
Minimal changes in the program should produce equally minimal diffs.
With modern text editors, Lisp programs are easy to edit. But often an equivalent of a one-line change in Python would create a multi-line diff in Lisp just because if you delete the last element of an S-expression you also have to move all the closing parentheses. This syntax proposal should aim at minimizing such effects.

---
Copyright (c) Ivan Babushkin.
