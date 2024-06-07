<!-- @format -->

## Title: Regex Tutorial: Matching URLs

## Introduction

Regular expressions (regex) are powerful tools for pattern matching and text manipulation. They provide a concise and flexible way to search for specific patterns within strings. In this tutorial, we will explore a regex pattern commonly used for matching URLs. By understanding the components of this regex, you will be able to validate and extract URLs from text effectively.

## Summary

The regex pattern we will be discussing is: `/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

This regex pattern is designed to match valid URLs. It allows for optional `http://` or `https://` protocol, followed by a domain name, a top-level domain (TLD) with a length of 2 to 6 characters, and an optional path and query string.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Author](#author)

## Regex Components

### Anchors

The regex pattern starts with the caret (`^`) anchor and ends with the dollar sign (`$`) anchor. These anchors ensure that the entire string matches the pattern from start to end.

### Quantifiers

The quantifier `{2,6}` is used to specify the length range for the top-level domain (TLD). It means that the TLD must have a minimum length of 2 characters and a maximum length of 6 characters. The quantifier `*` is used to match zero or more occurrences of the preceding group `([\/\w \.-]*)`, allowing for optional path and query string.

### Character Classes

The character class `\d` is used to match any digit character. It is equivalent to the bracket expression `[0-9]`. The character class `\w` is used to match any word character (alphanumeric characters and underscore).

### Grouping and Capturing

The regex pattern uses parentheses `()` to create capturing groups. There are four capturing groups in this pattern:

1. `(https?:\/\/)?`: Captures the optional protocol part of the URL.
2. `([\da-z\.-]+)`: Captures the domain name part of the URL.
3. `([a-z\.]{2,6})`: Captures the top-level domain (TLD) part of the URL.
4. `([\/\w \.-]*)*`: Captures the optional path and query string part of the URL.

### Bracket Expressions

Bracket expressions are used to define sets of characters that can be matched. In this regex pattern, we have two bracket expressions:

- `[\da-z\.-]`: Matches any digit, lowercase letter, dot, or hyphen.
- `[a-z\.]`: Matches any lowercase letter or dot.

### Greedy and Lazy Match

The regex pattern uses greedy matching by default. The quantifiers `*` and `{2,6}` are greedy, which means they will match as many characters as possible while still allowing the overall pattern to match.

## Author

This tutorial was written by Jake Pearson. You can find more of my work on my GitHub profile.
