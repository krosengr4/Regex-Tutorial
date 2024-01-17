# Title (replace with your title)

Regular expressions, known as Regex, is code that contains a series of special characters used to define a search pattern. At first regex may seem confusing and complicated, but when broken down into simple sections, regex becomes much more easy to understand. That is what I will be doing in this tutorial.

## Summary

The line of that I will use to break into smaller sections is below. 

```
/[\w._%+-]+@[\w.-]+\.[a-zA-z]{2,4}/
```
This is a regular expression that is used to match an email address.



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
Anchors are characters within the regular expressions that allow the user to match strings begin or end with certain characters.

- `^` matches any string that start with the anterior word.
- `$` matches a string that ends with the word infront of the character.
For example:
- Hello --- Would match any string with the exact text 'Hello' in it. 
- ^Hello --- Would match any string starting with the word 'Hello'.
- world$ --- Would match any string ending in 'goodbye'.
- ^Hello world$ --- Matches exactly 'Hello world'



### Quantifiers

Quantifiers are characters within the regular expression that specify how many instances a charcter, group, or character class must be represented in the input to be matched.

- `*` matches a string that has the anterior followed by zero or more of the last character. 
- `+` matches a string that has the anterior followed by one or more of the last character. 
- `()*` matches a string that has any anterior characters followed by zero or more copies of the string within the brackets.

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

- Kevin Rosengren is a junior developer in his bootcamp class hosted by the University of Texas at Austin.

Github profile: https://github.com/krosengr4
