# Email Validation Regex Tutorial

In this tutorial I will decode and explain the email matching Regex.
Regex, which is short for regular expression, is a sequence of characters that defines a specific search pattern. When included in code, regular expressions can be used to  to to do mant things such as find certain patterns of characters within a string. They are also frequently used to validate input, such as the email matching regex I will be showing you below.

## Summary

The following regular expression can be used to verify that user input is a valid email address- I will show you the Regex below and walk you through how it works by breaking it down into smaller pieces.
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors
The anchors used in this particular Regex were ^ and $.
`^` -Matches the start of the string.
`$` -Matches the end of the string.
Eg. `^Thanks$`

### Quantifiers
The quantifiers used in this particular Regex were + and {2,6}.
`+` -Matches the preceding element/token one or more times.
`{2,6}` -Matches the preceding element/token 2-6 times, the first number being the min and second being max.

### Grouping Constructs
This particular Regex contains three groups.
The first would be `([a-z0-9_\.-]+)`, this would be the first portion of an email e.g the portion before the @ symbol. This particular Regex allows this group to match lowercase letters from a-z, numbers from 0-9 and the particular special characters mentioned.
The second would be `([\da-z\.-]+)`, this would be the second portion of an email e.g the portion after the @ symbol- usually your email provider such as gmail, yahoo etc. This particular Regex allows this group to match any digit character (`/d`), lowercase letters from a-z as well as the special characters mentioned.
The third would be `([a-z\.]{2,6})`, this would be the end portion of an email- usually `com`. This particular Regex allows this group to match any lowercase letters from a-z and has a min length of 2 and a max of 6.

### Bracket Expressions
Bracket Expressions help to match a single character or collating elements eg. `([a-z0-9]+)`- this particular bracket expression allows lowercase characters from a-z and digits from 0-9. You can also use `\d` to match digits from 0-9 as well as the `\w` to match a-z, A-Z, 0-9, including _ (underscore).
### Character Classes
A character class is a set of characters that are within square brackets. It specifies the characters that will match a single character from a given input string.
E.g `([hierf])` will match lowercase h,i,e,r or f from the input string.
### The OR Operator
You can use the OR `|` operator to match characters or expression of either the left or right of the | operator. For example `(h|H)` will match either h or H from the input string.

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
