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
- [Use regex to match an Email Address](#use-regex-to-match-an-email-address)

## Regex Components

### Anchors

Anchors are what defines the start and finish of the parameters you are searching for. 
<br/>

For example the "^" character signifies the start of the parameters you wish to search for and the "\$" closes the permitters to search within. The code or parameters that are written between "^" and the "\$" characters are what defines the search and will match a line, word or even a string.

For example: The following regex will match any string that starts with "G'day":

```
/^G'day$/
```

### Quantifiers

Quantifiers set the parameters of your search. It does this by limiting the string that your regex matches, this can be be set to limit sections of the string too. For example, the "*" quantifier matches zero or more occurrences of the preceding character, while the "+" quantifier matches one or more occurrences, and "?" qualtifier matches zero or one time.

Example code snippet: The following regex will match any string that contains digits with a length of 3 or more:
```
/\d{3,}/
```

### OR Operator
In Regex the "|" character stands for "or" and is used in the same way as your would in a JavaScript for loop. This function allows to match one of many alternatives.
Example code snippet: The following regex will match either "Ferrari" or "McLaren":
```
/Ferrari|McLaren/
```

### Character Classes

Character Classes are used to define a set of characters in Regex that you wish the search to return. An example of character classes includes all lowercase letters, all white spaces, or all digits.
Example code snippet: The following regex will match any string that contains a vowel:
```
/[aeiou]/
```

### Flags

Flags are the only exception to the Regex rule where a character may be placed outside of the slash characters that define the search. The are only 6 optional flags  and may change the behaviour of your search/match such as making it case-insensitive, multi-line searches and even a global search.

Example code snippet: The following will match any string that contains the word "banana", regardless of case:
```
/banana/i
```

### Grouping and Capturing

Grouping and Capturing in Regex allows you to capture sections and group them together as part of your search. To do this, parentheses (()) are used for each section you wish to check for and capture. This is also commonly referred to as "subexpressions" 

Example code snippet: The following regex will match a valid email address, username and domain:
```
/(\w+)@(\w+\.\w+)/
```

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

Boundaries are used to match patterns at specific positions, such as the beginning or end of a word.
Example code snippet: The following Regex will match any word that ends with "i" such as Ferrari:
```
/i$/
```

### Back-references

Back-references refers to a previously captured group in the same regular expression.

Example code snippet: The following regex will match any string that contains a repeated word:
```
/\b(\w+)\b.*\b\1\b/
```

### Look-ahead and Look-behind

The Look-ahead and Look-behind assertions allow to match a search only if it is followed or preceded by another pattern. This feature is particularly handy if you are looking for a particular full name within an array of names, allowing for a more specific search.

Example code snippet: The following regex will match any string that contains "michael" followed by "schumacher":
```
/michael(?=.*schumacher)/
```

### Use Regex to match an Email Address

Lets break down how to use Regex to match an email address using the following code:
```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

* Firstly the caret character "^" at the beginning of the expression above indicates the start of the string to be matched.
* Secondly parentheses are used to group parts of the expression together. In this case, there are three groups which are separated by the "@" symbol and the "." symbol.
* [a-z0-9_.-]+ matches one or more characters that are either lowercase letters, digits, underscores, periods, or hyphens. This is the first group of characters in the email address, before the "@" symbol.
* Next the "@" symbol is a literal character that must be present in the email address.
* [\da-z.-]+ matches one or more characters that are either digits, lowercase letters, periods, or hyphens. This is the second group of characters in the email address, after the "@" symbol and before the "." symbol.
* As with the "@" character the literal "." (period) character must be present in the email address.
* The last variable that the search will match for is [a-z.]{2,6} and matches between 2 and 6 characters that are either lowercase letters or periods. This is the third and final group of characters in the email address, after the "." symbol.
* Lastly the dollar sign "$" at the end of the expression indicates the end of the string to be matched.
<br/>

It's also worth noting that *Flags* would not be used in this search due to the very nature of an email address having so many variables.


## Author

My name is Ben Armstrong and I am currently attending a Full Stack Web Development Bootcamp through The University of Adelaide.
Feel free to look at my other work on GitHub: [https://github.com/BenArmstrong81]( https://github.com/BenArmstrong81)