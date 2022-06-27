# Regex Tutorial: Email Matching

This gist is a tutorial writeup on a specific regex, or regular expression, based on matching an email. A regular expression is a sequence of characters that defines a specific search pattern. In code, a regex can be described simply as pattern matching of characters within a string to help validate input.

## Summary

Within this tutorial I will break down the components which make up the regular expression used to validate an email address. We can best look at regex in code groupings, breaking down each segment of the regex to help us explain its functionality. The following code snippet seen below is the regex in question:  

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`  

The first grouping component can be broken down as follows:
`([a-z0-9_\.-]+)`
- `a-z`  The string can contain any lowercase letter between a-z.
- `0-9`  The string can contain any number between 0-9.
- `_\.-`  The string can contain an underscore, period, or hyphen.
- `+`  The pattern of the preceding string must be matched one or more times.
Then the string must include the @ symbol.`@`  

The second grouping component can be broken down as follows:
`([\da-z\.-]+)`
- `\d`  The string can include any number 0-9. The \d simply represents a digit 0-9. 
- `a-z`  The string can include any lowercase letter a-z.
- `\.-`  The string can include a period or hyphen.
- `+`  The pattern of the preceding string must be matched one or more times.
Then the string must include a period.`\.`  

The last grouping component can be broken down as follows:
`([a-z\.]{2,6})`
- `a-z`  The string can contain any lowercase letter between a-z.
- `\.`  The string can include a period.
- `{2,6}`  The preceding string must be between 2 and 6 characters in length.  

I will further break down the components of this regex in the sections below: 

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

### Quantifiers

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

Please reach out to me at the contact information provided below:

View my GitHub Profile: [MNlegion](https://github.com/MNlegion)

Contact me: rkreuser30@gmail.com
