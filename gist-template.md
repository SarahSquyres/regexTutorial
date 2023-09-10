# Regex Tutorial: Matching URL

Regular expressions, or regex, are useful for dynamic string searches.  Where methods and IF statements fall short, regex can get the job done.

For instance, if we need to match a username, a regex such as this may come in handy:

`/^[a-z0-9_-]{3,16}$/`

The above regex checks to see if a string fulfills the requirements for a basic username.  The string can:
* have lowercase letters between a-z
* be any number between 0-9
* contain an underscore or hyphen
* and be between 3-16 characters long

Now that you have a general understanding of the purpose and syntax of regex, let's take a deeper look into the different components.

## Summary

In order to better understand regex and it's components, we will be dissecting the following expression:

`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

This regular expression is used to verify if a given string is valid a URL.  The overall functionality of the regex is as follows:

- `^` indicates the beginning of the string
- `(https?:\/\/)?` states the URL protocol can either be `http://` or `https://` and the `?` allows the protocol to be optional
- `([\da-z\.-]+)` looks for the domain name and states it can contain alphanumeric characters, `.` and `-`
- `\.([a-z\.]{2,6})` is the ".com" or ".org" portion of the URL and can contain lowercase letters and `.` as long as the characters are between two and six characters in length
- `([\/\w \.-]*)*` allows `/`, alphanumeric characters, `.` and `-` zero or more times
- `\/?` makes the trailing `/` optional
- `$` indicates the end of the string

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Author](#author)
- [Credits](#credits)

## Regex Components


### Anchors
The anchors for our expression are `^` and `$`, and are placed at the beginning and end of the expression. Everything between these two symbols will be validated. It is important to note that regex is case sensitive when you are formulating your expression.


### Quantifiers
Our expression also contains the quantifiers `?`, `+`, `*` and `{}`. Quantifiers are used to specify the number of times a character or pattern should be present to match the specified search. 

For our purposes, the `?` is used to "match the pattern either zero or one time."  In other words, in the grouping `(https?:\/\/)` it is not required for the request to begin with either `http` or `https`. The `+` is used in reference to the `[\da-z\.-]` pattern, allowing it to be matched one or more times. `*` allows a match zero or more times. The `{}` are also used.  In our expression, `{2,6}`, allows the pattern, `[\a-z\.-]`, to match between 2 and 6 times.


### OR Operator
We have several `\` (OR operators) in our code. 

With OR operators, the pattern on either the left or the right can return a match.  This is illustrated in our code, `[a-z\.]` means any lowercase letter or a `.` will match.


### Character Classes
Character classes are enclosed in `[]` and are used to define a set of characters that can be matched.

Our expression uses character classes throughout. For example, in the pattern `[\da-z\.-]`, the character class matches any alphanumeric character OR a `.` or `-`.  Character classes are used again in the pattern `[a-z\.]` matches any lowercase letter or `.`. Finally, the pattern `[\/\w \.-]` matches any combination of `/`, word character, `.` or `-`.


### Grouping and Capturing
Grouping is indicatied with `()` and is used to define subexpressions. Subexpressions look for an exact match to the specified pattern.

Our code has specified four groupings: 

- `(https?:\/\/)`, matches the `http` or `https` protocol

- `([\da-z\.-]+)`, matches any alphanumeric character, `.` or `-` and can be matched once or more

- `([a-z\.]{2,6})`, matches any lowercase letter or `.` between two and six times

- and `([\/\w \.-]*)` matches `/`, word character, `.` or `-` zero or more times


### Bracket Expressions
Bracket expressions are a type of character class. We discussed the use of `[]` previously, but to review they encapsulate characters that can be matched.


### Greedy and Lazy Match
Quantifiers are greedy by nature, the goal being to match as many patterns as possible.  In contrast, lazy quantifiers match the fewest characters possible. To make a quantifier lazy, add the `?` afterward. 


## Author
Hi! My name is Sarah. I am a full-stack developer. Thanks for reading my tutorial!

GitHub Profile: https://github.com/SarahSquyres 

## Credits
Xpert Learning Assistant

https://bard.google.com/ 

https://coding-boot-camp.github.io/full-stack/computer-science/regex-tutorial 
