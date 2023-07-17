# Strong Password Regex Tutorial

Hello and welcome to my tutorial on Regex! This specific tutorial will help you create and verify strong passwords!

## Summary

In this tutorial you will learn regex and how it can be used to create and verify strong passwords. Below is an example Regex which checks to make sure a lower case value, upper case value, a numebr from 0-9 and a special character was used and that it is at least 8 characters long:

(?=^.*[a-z])(?=.*[A-Z])(?=.*[0-9]).*$(?=.*[^A-Za-z0-9])(?=.{8,})

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components
Regular Expressions (Regex) are patterns of characters that are used to match combinations in strings. These patterns consist of one or more character literals, operators or constructs.

### Anchors
In all regular expressions (regex), a ^ indicates what the password string should start with and a $ indicates what the string should end with.
For example, if we scramble the example string above:

(?=^.*(?=.*[0-9])([a-z])(?=.*[A-Z]$)(?=.*[^A-Za-z0-9])(?=.{8,})

The ^ indicates that the password must start with an integer for 0-9 and the $ indicates that the password should end with a capitalized character set.

### Quantifiers
In regex, quantifiers indicate the number of characters or expressions to match in the string.
Some examples:
The '*' : Star, Matches 0 or more of the preceding characters
{8} : Specific Quantifier, Matches from 6 to 10 of the preceding characters

In the example above where the * is placed says that there must be more than 0 of the the characters and integerse and the {8,} says that the password has to be 8 characters long from the characters and integers expressed in the string.

### Character Classes
With character classes in regex, you are able to tell the regex to match one of several characters that you provide. 
In our expression above we say [a-z], meaning we must match one character in lower case from a-z. If we said [b-g], the regex engine would only accept one character in lower case between b-g.
The '.' tells the regex engine to match any character inside the character set [].

### Grouping and Capturing
The parentheses, (), groups the text together. 
Example: 
(?=.*[^A-Za-z0-9]) - groups UPPER case characters, lowercase characters and numbers between 0-9 together to form a password.

### Look-ahead and Look-behind
The lookahead syntax, (?=) madds a condition for what follows. So, in the example: (?=foo), the engine would process "foo" 

## Author
Thank you for reading this Regex tutorial on how to create a strong password! I am currently a Cybersecurity Engineer for a national retail chain and a student at the U of M in the Full Stac Web Development course. Please take a look at my github to see my work or get inspiration for projects:

https://github.com/erbester51 
