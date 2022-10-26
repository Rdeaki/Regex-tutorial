# What is Regex?

The best way i've seen regex summarized is "a string on steroids". A Regular expression is essentially a pattern that is matched against a subject string from left to right. Examples Regular expression uses are; to replace text within a string, validate forms, extract a substring from a string based on a pattern match, and many many more use cases. Developers love their abreviations, so the mouthful "regular expression" gets shortened to "regex" or "regexp".

## Password pattern matching

I know everyone under the age of 105 has seen the message: "Your password must contain at least 8 characters, an upper case letter, and a number." Aside from casuing you to forget the password immediatly after creating your account, this phrase also describes a pattern you need to follow in order for you to provide a valid password. From a developers perspective, you could write some javascript to validate the users input OR you could write a single line of code to descibe the entire pattern. Take it away Regex:

```
/^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*\W).{8,}$/g
```

        Include a code snippet of the regex. Replace this text with your summary.

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

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
