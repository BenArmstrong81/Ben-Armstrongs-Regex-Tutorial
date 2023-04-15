# Ben Armstrong's Regex Tutorial

Regular Expression, or, more commonly referred to as “Regex” is a powerful tool that is used in many programming languages and text editors that uses a sequence of characters for patter matching and string manipulation.
This Regex Tutorial covers the syntax and basic concepts of Regex, as well as examples of common use cases, tips for writing efficient and effective regular expressions.


## Summary

In this tutorial I will cover off on the following eleven main Regular Expressions (Regex) components; Anchors, Quantifiers, OR Operators, Character Classes, Flags, Grouping and Capturing, Bracket Expressions, Greedy and Lazy Matching, Boundaries, Back-references, and Look-ahead and Look-behind.

An example code for each will be provided along with a brief summary of how/what each is used for. The aim is to provide you with a solid foundation so that you gain an understanding of the most commonly used regex components and how to use them effectively in your own projects. 
I hope you enjoy reading as much as I did creating this for you!


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

Anchors are what defines the start and finish of the perameters you are searching for. 
For example the "^" character signifies the start of the perameters you wish to search for and "$" closes the permaters to search within. The code or perameteres that are written between "^" and "$" are what defines the search and will match a line, word or even a string.

For example: The following regex will match any string that starts with "G'day":

```
/^G'day$/
```

### Quantifiers

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

Bracket Expressions allow to match a range of characters and are is commonly referred to as a Positive Character Group. The search is performed within square brackets ([]) and allows you to search for characters such as all uppercase letters or all punctuation marks.

Example code snippet: The following regex will match any decimal digit:
```
/[0-9]/
```

Another Bracket Expression example code snippet: The following regex will match any whitespace characters, including line breaks
```
[ \t\r\n\v\f]
```


### Greedy and Lazy Match

The 'Greedy' expression refers to matching the longest pattern possible. And 'Lazy' expression is the opposite, matching the smallest pattern as possible.

Example code snippet: The following 'Lazy' regex will match the shortest possible string that starts with the letter "b" and ends with "a":
```
/b.*?a/
```
*So it would return Banana and NOT Bananas*


### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

My name is Ben Armstrong and I am currently attending a Full Stack Web Development Bootcamp through The University of Adelaide.
Feel free to look at my other work on GitHub: [https://github.com/BenArmstrong81]( https://github.com/BenArmstrong81)