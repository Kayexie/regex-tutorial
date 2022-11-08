# Regex Tutorial of Email Address

A regular expression, shortened as regex, is a search pattern of text. It includes both common characters(eg. numbers and letters) and special characters ('meta characters'). Regex is used to retrieve and replace text that matches a search pattern.

## Summary

This tutorial is going to use a regex to match an email address. An email address consists of local part, @ symbal, domain and extension. The local part can includes letters(uppercase or lowercase), numbers and some special characters(eg.-_.). Doman has letters, numbers or hyphen and extension only contain letters. <br />Below regex is going to be used as an exapmle: <br />
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors
/`^`([a-z0-9.-]+)@([\da-z.-]+).([a-z.]{2,6})`$`/ <br />
`^` and `$` are both defined as anchors in regex. `^` indicates the begining position of the string unless used in a squre bracket. On the contratry, `$` is used to indicates the ending position of the string. Here in the example, the string must start with something matches ([a-z0-9.-]+) and end with the pattern of ([a-z.]{2,6}).

### Quantifiers 
/^([a-z0-9.-]`+`)@([\da-z.-]`+`).([a-z.]`{2,6}`)$/ <br />
Quantifiers are defining the length of the characters. `+` here means the string must match the pattern any of [[a-z0-9.-] at least one time or even more. `{}` provide a scope of how many times the pattern should appears. for example, `{2,6}` means the string must match the pattern at a minimun of 2 and maximum of 6 times. 

### Character Classes
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ <br />
`a-z`, `0-9` is searing for letters from a to z and numbers 0-9. `\d` also means the number of 0 to 9 but only a single digit.

### Grouping and Capturing
/^`([a-z0-9_\.-]+)`@`([\da-z\.-]+)`\.`([a-z\.]{2,6})`$/ <br />
Grouping constructs is used to breake the string into different sections using `()` when the string is complex. The first group is `([a-z0-9_\.-]+)`, which is used to match the local part of the email address. The second section `([\da-z\.-]+)` is to detemine the domain.
`([a-z\.]{2,6})` is to match the extension.

### Bracket Expressions
/^(`[`a-z0-9_\.-`]`+)@(`[`\da-z\.-`]`+)\.(`[`a-z\.`]`{2,6})$/<br />
The `[``]` would include any required characters that we want to match within the email address.
a-z: letters from a to z;
0-9: numbers from 0 to 9;
_,\.,-: the local parts of the email address could be able to contain these symbols. The backslash of the period is Escape character.

### Greedy and Lazy Match
/^([a-z0-9_\.-]`+`)@([\da-z\.-]`+)`\.([a-z\.]`{`2,6`}`)$/ <br />
Quantifiers are greedy. They would do the match as many as possible.

## Author
Kaye Xie<br />
GitHub Profile: https://github.com/Kayexie.
