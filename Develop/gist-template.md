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
Notice the `/` characters which wrap our regex. This is due to the regex being considered literal.

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

### Anchors
Two characters define the anchors of the regex. These are the `^` and `$` characters. The `^` anchor marks the beginning of the string while the `$` marks the end of the string. You can see each of these anchors functioning within our regex (reference below). Quantifiers are not included in this string, even though they fall between the two anchors.

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

### Quantifiers
Quantifiers are used to specify how many times the pattern is matched. In the matching email regex, there are a few different quantifiers being used. The first that occurs is the plus `(+)` quantifier. This matches the pattern that precedes it one or more times. Then there is the curly bracket `({})` quantifier that can set limits for a match. The curly bracket quantifier in the matching email regex can be found at the end of the expression as seen below. In our example, `{2,6}` means that the preceding string is matched a minimun of 2 times and a maximum of 6 times.   

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing
Grouping uses parentheses (()) to group different components of the string together to check and make sure they are fulfilling the requirements set for them. Below we can see the three different constructs within our email regex below:   

`([a-z0-9_\.-]+)`  

`([\da-z\.-]+)`  

`([a-z\.]{2,6})`

Full regex reference: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

### Bracket Expressions
Bracket expressions can be used to match allowable characters. Anything inside of the set of square brackets ([]) will represent the chararcters that are being matched. The first of these encountered in this particular regex is `[a-z0-9_\.-]`, which allows lowercase letters a-z, numbers 0-9, `_`, a literal `.` punctuation mark, or a `-`. In the matching email regex, there are three different bracket expressions as you can see broken down individually below:

`[a-z0-9_\.-]`  

`[\da-z\.-]`  

`[a-z\.]`

Full regex reference: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

Please reach out to me at the contact information provided below:

View my GitHub Profile: [MNlegion](https://github.com/MNlegion)

Contact me: rkreuser30@gmail.com
