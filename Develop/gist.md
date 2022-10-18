Regex Tutorial - Matching an Email

A regex, which is short for regular expression, is a sequence of characters that defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also frequently used to validate input. 

This tutorial will focus on how to match an email using regular expression. 

## Summary

This tutorial will show you how to match emails using the expression /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/. This can be useful to verify that a user input is a valid email address using applications/technologies such as Node or MongoDB. 

Each component of this regex has a unique responsibility to make sure that a user enters an email address that begins with an unspecified number of characters preceding the @ symbol, followed by a domain.

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
Regres anchors match a position before or after characters. In this instance, the anchor used for matching an email is ^ (the begining of the string or line) and $ (the end of the string or line). 

### Quantifiers
Quantifiers match a number of instances of a character, group, or character class in a string. When matching an email, the + operator connects the users email username + email domain + .com. Additionally, this regex includes {2,6}, which will allow a match range of 2-6 characters for the character set of [a-z\.].

### Character Classes
The character class in this regrex is \d which matches a single character to any digit from 0-9.

### Grouping and Capturing
Anything within () is taken as a group. Between /^ and $/, there are three distinct character groups, ([a-z0-9_.-]+), ([\da-z.-]+), and ([a-z.]{2,6}). If we took away the internal logic, it would look like (1)@(2).(3), which follows the email format (string)@(website).(com/edu/etc).

### Bracket Expressions
A bracket expression represents a single character. There are three within our code: [a-z0-9_.-], [\da-z.-], and [a-z.]
Combined with the quantifier +, any number of characters matching those specified within the brackets will match. Note: bracket expressions are case sensitive. 

### Greedy and Lazy Match
This regrex includes two greedy matches. The + quantifier will match as many times as possible and the {} is another greedy match that's used when matching {2,6} for the last capture group.

## Author
Hanna Marcus is a Web Developer living in San Francisco, CA. You can find her GitHub profile here: https://github.com/hannamarcus 