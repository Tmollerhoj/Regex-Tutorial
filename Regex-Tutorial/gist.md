# RegEx Tutorial

In this tutorial we will be going over the uses and functionality of regex. If you don't know what that means yet, read on.

## Summary

Regex, or regular expression, refers to an assortment of characters used to create a matching pattern in strings. It is often used in string searching algorithms and input validations such as when searching for key-words or creating passwords respectively.

In this tutorial we will deconstruct a piece of code to better understand how regex works.

Example email regex: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

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

Anchors are used to mark ^ the beginning and $ end of the string being matched. 

If we look at our email regex we can see how it is used in the following:

^([a-z0-9_\.-]+) Marks the beginning of our regex.

([a-z\.]{2,6})$ Marks the end of our regex.

### Quantifiers

Quantifyers help the code understand how many it should be looking to match of a preceeding character or group of characters. 

Quantifiers include "+" matching 1 or more, "*" matching 0 or more, "?" matching 0 or 1, and "{}" matching specific perameters. Brackets can be used as { n }, { n, }, or { n, m } matching an exact n number of times, n or more times, and between n and m times respectively.

[a-z0-9_\.-]+ Matches whats in the brackets 1 or more times.

[\da-z\.-]+ Matches whats in the brackets 1 or more times.

[a-z\.]{2,6} Matches whats in the brackets between 2 and 6 times. 

### OR Operator

The OR operator "|" allows the use of two different regex and returns a match if either of one of them work. 

However, our example does not use it.

### Character Classes

Character classes defines sets of characters in our regex that can return a match.

Some common character classes include "." matching any character, "\d" matching numerical characters, "\w" matching alphanumeric characters, and "\s" matching white spaces. These last three can be inversed by simply capitalizing. "\S" would match everything but white spaces.

In our regex "\d" would match numerical characters after the "@".

### Flags



### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
