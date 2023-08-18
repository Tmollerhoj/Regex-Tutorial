# RegEx Tutorial

In this tutorial we will be going over the uses and functionality of regex. If you don't know what that means yet, read on.

## Summary

Regex, or regular expression, refers to an assortment of characters used to create a matching pattern in strings. It is often used in string searching algorithms and input validations such as when searching for key-words or creating passwords respectively.

In this tutorial we will deconstruct a piece of code to better understand how regex works.

Example email regex: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

Anchors are used to mark `^` the beginning and `$` end of the string being matched. 

If we look at our email regex we can see how it is used in the following:

`^([a-z0-9_\.-]+)` Marks the beginning of our regex.

`([a-z\.]{2,6})$` Marks the end of our regex.

### Quantifiers

Quantifyers help the code understand how many it should be looking to match of a preceeding character or group of characters. 

Quantifiers include `+` matching 1 or more, `*` matching 0 or more, `?` matching 0 or 1, and `{}` matching specific perameters. Brackets can be used as `{ n }`, `{ n, }`, or `{ n, m }` matching an exact n number of times, n or more times, and between n and m times respectively.

`[a-z0-9_\.-]+` Matches whats in the brackets 1 or more times.

`[\da-z\.-]+` Matches whats in the brackets 1 or more times.

`[a-z\.]{2,6}` Matches whats in the brackets between 2 and 6 times. 

### OR Operator

The OR operator `|` allows the use of two different regex and returns a match if either of one of them work. 

However, our example does not use it.

### Character Classes

Character classes defines sets of characters in our regex that can return a match.

Some common character classes include `.` matching any character, `\d` matching numerical characters, `\w` matching alphanumeric characters, and `\s` matching white spaces. These last three can be inversed by simply capitalizing. `\S` would match everything but white spaces.

In our regex `\d` would match numerical characters after the `@`.

### Flags

Flags are modifiers that alter how a regex pattern is interpreted, and are placed after the second slash. They can change the behavior of the pattern matching process. Common flags include `g` global search, `i` case-insensitive search, and `m` multi-line search.

However, we do not use flags in our regex.

### Grouping and Capturing

Grouping is essentially the use of parenthesis to group patterns together to create subexpressions, use quantifiers, or to capture text for matching. In our email example it is mainly used for creating subexpressions to better organize our regex.

`([a-z0-9_\.-]+)`

`([\da-z\.-]+)`

`([a-z\.]{2,6})`

### Bracket Expressions

Bracket expressions are actually a part of character classes. By using `[]` we define a range of characters accepted by our regex. 

For Example:

`[a-z0-9_\.-]` Matches alphanumeric characters, periods and dashes.

`[\da-z\.-]` Matches alphanumeric characters, periods and dashes.

`[a-z\.]` Matches alphabetic characters and periods.

### Greedy and Lazy Match

By default regex is greedy, matching as many instances as possible. By using the quantifier `?` it becomes lazy because it only matches  0 or 1 times. However, it is not used in our example.

### Boundaries

The boundary or `\b` is an anchor like `^` and `$`, but it is used specifically to mark the boundaries of words. However, it is not used in our example.

### Back-references

Back-references allow you to refer to previously captured groups within the regex pattern. However, it is not used in our example.

### Look-ahead and Look-behind

Look-ahead and look-behind assertions allow you to check for patterns that are followed by or preceded by another pattern, without including the latter in the match. However, it is not used in our example.

## Author

Thomas Mollerhoj

https://github.com/Tmollerhoj
