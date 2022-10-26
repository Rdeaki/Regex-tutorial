# What is Regex?

The best way i've seen regex summarized is "a string on steroids". A Regular expression is essentially a pattern that is matched against a subject string from left to right. Examples Regular expression uses are; to replace text within a string, validate forms, extract a substring from a string based on a pattern match, and many many more use cases. Developers love their abreviations, so the mouthful "regular expression" gets shortened to "regex" or "regexp".

## Password pattern matching

I know everyone under the age of 105 has seen the message: "Your password must contain at least 8 characters, an upper case letter, and a number." Aside from casuing you to forget the password immediatly after creating your account, this phrase also describes a pattern you need to follow in order for you to provide a valid password. From a developers perspective, you could write some javascript to validate the users input OR you could write a single line of code to descibe the entire pattern. Take it away Regex:

```
/^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*\W).{8,}$/g
```

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

/`^`(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*\W).{8,}$`/`g

Anchors in regular expressions serve as indicators for the beginning and the end of a regex.

- The `^` represents the beginning of a string or line.
- The `$` represents the end of that string/line.

### Quantifiers

/^(`?`=.`*`[a-z])(`?`=.`*`[A-Z])(`?`=.`*`\d)(`?`=.`*`\W).`{8,}`$/g

Quantifiers indicate that the preceding character must be matched a certain number of times. Essentially how many characters we need. By default quantifiers are "greedy" and will try to match as many characters as possible, unless specified.

- `{8,}` Matches the specified quantity of the previous character. {8,} will match to 8 or more characters.
- `?` effectively makes the character optional. In our instance the option will be lowercase, uppercase, and number options for our passowd.
- `*` Matches 0 or more of the preceding character.

### Character Classes

/^(?=`.`*`[a-z]`)(?=`.`*`[A-Z]`)(?=`.`*`\d`)(?=`.`*`\W`)`.`{8,}$/g

- `[a-z]` , `[A-Z]` matches any characters within the specified range. In our instance its any lower or upcase letter in the alphabet.
- `.` indicates that a character must have something before or after it. AKA no spaces allowed in our password.
- `\W` matches any non alphabetical word character (a-z), example characters (!,^#$@)
- `\d` matches any numeric value (0-9)

### Greedy and Lazy Match

greedy and lazy dictate what is returned from a matching pattern. As mentioned above, by default quantifiers are greedy. `*` is the default greedy, it will continue for each subsequent matching charcater. `?` will stop after the first instance.

### Look-ahead and Look-behind

/^`(?=.*[a-z])``(?=.*[A-Z])``(?=.*\d)``(?=.*\W)`.{8,}$/g

There's a few different lookaround operators, but for our instance well focus on one. The highlighted regex snippets above are posotive lookaheads, they match a group after the main expression without including it in the result. A simple way to break it down: `X(?=Y)` will match any instance of X that is followed by Y.



## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
