# Regex Tutorial: Matching URL

Regular expressions, or regex, are useful for dynamic string searches.  Where methods and if statements fall short, regex can get the job done.

For instance, if we need to match a username, a regex such as this may come in handy:

`/^[a-z0-9_-]{3,16}$/`

The above regex checks to see if a string fulfills the requirements for a basic username.  The string can:
* have lowercase letters between a-z
* be any number between 0-9
* contain an underscore or hyphen
* and be between 3-16 characters long

Now that you have a general understanding of the purpose of regex, let's take a deeper look into the different components.

## Summary

In order to better understand regex and it's components, we will be dissecting the following expression:

`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`



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
