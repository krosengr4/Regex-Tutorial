# Regex (Regular Expression) Tutorial

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

<hr>

## Regex Components

<br>

## Anchors
Anchors are characters within the regular expressions that allow the user to match strings begin or end with certain characters. The characters `^` and `$` are considered to be anchors.

- `^` matches any string that start with the anterior word.
- `$` matches a string that ends with the word infront of the character.

In other words, The `^` signifies the start of the string and the `$` signifies the end of the string.

For example:
- Hello --- Would match any string with the exact text 'Hello' in it. 
- ^Hello --- Would match any string starting with the word 'Hello'.
- goodbye$ --- Would match any string ending in 'goodbye'.
- ^Hello goodbye$ --- Matches exactly 'Hello goodbye'

<br>

## Quantifiers

Quantifiers set the limits of the string that the regex matches. Special characters within the regular expression set the minimum and maximum number of characters of the string that the regex matches.

- `*` matches a string that has the anterior followed by zero or more of the last character. 
- `+` matches a string that has the anterior followed by one or more of the last character. 
- `()*` matches a string that has any anterior characters followed by zero or more copies of the string within the brackets.

<br>

## OR Operator

An OR operator, often marked with a `(|)` or `[]`, matches on a choice of regular expressions. If you put the character(s) representing the OR operator between any two characters in the regular expression, the regex will match the union of the strings that those two characters match. 

An expression written `[abc]` could be written as `(a|b|c)`, which means `(a OR b OR c)`.

Examples: 
* `(|)` - mathces a string that has any anterior characters followed by the characters on the left or right of the vertical bar.
* `[]` - matches a string that has any anterior characters without any characters within the brackets.

<br>

## Character Classes

A character class in a regex defines a set of characters, any one of which can occur in an input string to fulfill a match. They often begin with a `\` followed by a character. Character Classes tell the regex engine to match only one specific characters out of many.

Examples:
* `\d` - matches a single character that is a digit
* `\w` - matches a word character (any alphanumeric character plus underscore)
* `.` - matches any character

<br>

## Flags

Flags are used to make changes to the default behavior on how a Regex searches a string. They are placed at the end of a regular expression and they define additional functionality or limits for how the regex searches.

examples: 
* `g` - Global search. the regex should be tested for all possible matches of a string
* `i` - Case *Insensitive* search. the case (upper/lower) should be ignored while attempting to match
* `m` - Multi line search. Will match the start and end of a line, and multiple lines, rather than just a string.

<br>

## Grouping and Capturing

Grouping or capturing groups allows one to combine selected characters or strings into a single unit. In other words, grouping or capturing groups unifies a pattern or string so that it is matched in a group.

To use capture groups, we can use `()` parentheses to create a capture group. We can also use `(?<>)` to put a name into the capture group. Also we can use `(?:)` to disable the capture group.

For example: 
* `x(xyz)` - Create a capture group with the value of 'xyz'.
* `x(?:xyz)` - Disable the capture group with the value of 'xyz'.
* `x(?<bar>xyz)` - Add name 'bar' to capture group with the value of 'xyz'.

<br>

## Bracket Expressions

Bracket Expressions are any characters that are inside of a bracket `[]` which represent a range of characters that are meant to match. In other words, Bracket Expressions are used to match any single characters within the brackets.

To use Bracket Expressions we use `[]` to match any character within the brackets. We can also user `[]%` to match the string within the brackets. In addition we can use `[^]` to match any string that *does not* contain a letter from the brackets, known as negation of expression.

For example: 
* `[xyz]` - matches a string that either has 'x' OR 'x y' OR 'x z'. 
* `[0-9]%` - A string that has a character from 0-9 before a %.
* `[^a-zA-Z]` - A string that *does not* contain a letter from z-a or from A-Z.

<br>

## Greedy and Lazy Match

Quantifiers can be made lazy by adding the `?` symbol at the end. This means that it will match as few occurences as possible.

However, when only dealing with greedy quantifiers, a `+` and/or `{}` can be used which allows the matches to expand as long as its needed.

* Greedy match = Quantifiers will attempt to match as *many* occurences of input possible.
* Lazy match = Quantifiers will attempt to match as *few* occurences of input possible.

For example: 
* `<.+?>` - matches any character that is included one or many time inside the '<' and '>'. Expands as needed.
* `<[^<>]+>` - matches any character expects `<` or `>` one or more times included inside `<` and `>`. 


<br>

## Boundaries

Boundaries can be used to capture specific instances or changes withing a designated string. They make assertions about what can be matched to the left and right of the current position.
Word boundaries are useful when you want to match a sequence of letters, or numbers, on their own.

<br>

## Back-references

Back-references are references to previously created/captured groups. Think of it as a way to reuse previous tags or lines of text. In addition, back-references also ensure two pieces of a string match.

Back-references are specified by using a `\` followed by a digit. 

For example:
* `([xyz])\1` - Using the `\1`, the regex matches the same text that was matched in the first capture group.
* `([uwx])([yz])\2\1` - We can use `\1`, `\2`, `\3` etc... to identify the same text that was captured in the 1st, 2nd, 3rd, ... capturing.

<br>

## Look-ahead and Look-behind

Look behind means to look at the word at the end of a specified sentence. Look ahead is the opposite, meaning to look at the word at the beginning of a specified sentence. 

To use look behind, you would use the syntax `(?<=Y)` where Y is your specified sentence. For look ahead you would use the syntax `x(?=Y)` where Y is the specified sentence.

For example: 
* `(?<=The Cat is Fuzzy.)*` - Look behind: The results will highlight the word `Fuzzy` as it is the last word in the sentence.
* `(?=The Cat is Fuzzy.)*` - Look ahead: The results will highlight the word `The` as it is the first word in the sentence.

<br>

## Author

 Kevin Rosengren is a junior developer in his bootcamp class hosted by the University of Texas at Austin.

 Github profile: https://github.com/krosengr4
