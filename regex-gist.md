## Regular Expressions
Regular expressions, or regex, are a sequence of characters that defines a set of search parameters. They are extremely versatile and customizable, so they are an important tool for any developer to know how to use.

## Summary
A regex "regular expression" is a sequence of characters that forms a search pattern. It is a powerful tool used in computer programming and text processing for finding and manipulating text strings.

Regex can match complex patterns in text, such as a certain sequence of characters, digits, or special characters. It can also be used to validate input or to search for specific text in a file.

Regex syntax can vary slightly depending on the programming language or tool being used, but the basic concept remains the same. It involves using metacharacters, which have special meaning, to create a pattern that matches the desired text.The regex we are going over today is, /^#?([a-f0-9]{6}|[a-f0-9]{3})$/i . This is the regex for matching a hex value.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Charecter Classes](#character-classes)
- [OR Operator](#or-operator)
- [Flags](#flags)
- [Character Escapes](#character-classes)

## Anchors
Anchors are used to specify where in the string the pattern should match, either at the beginning or end of the string or at a word boundary.

The "^" anchor is a start-of-line anchor, which indicates that the pattern must match at the beginning of the string. The "$" anchor is an end-of-line anchor, which indicates that the pattern must match at the end of the string. Together, they ensure that the regex matches the entire string, from the beginning to the end.

The "$" anchor is used at the end of the regex to ensure that the pattern ends at the end of the string. It matches the end of the line and ensures that the regex pattern matches until the end of the string.

## Quantifiers
A quantifier specifies the number of times a character or group of characters should be matched. Quantifiers are represented by special characters such as "*", "+", "?", and "{}".


The quantifier used is "{}". Specifically, the expression [a-f0-9]{6} is enclosed in curly braces to indicate that the preceding character class should be matched exactly six times, while the expression [a-f0-9]{3} should be matched exactly three times. These quantifiers ensure that the regex matches either a six-digit or three-digit hexadecimal color code and not more or less than six or three hexadecimal digits.

## Grouping Constructs
A grouping construct in a regex is a way to group together one or more parts of a regular expression and apply a specific operation to the entire group. In the context of regular expressions, grouping constructs are often used to create subexpressions that can be treated as a single unit. In the above hex regex the grouping construct is represented by the parentheses around the subexpression [a-f0-9]{6}|[a-f0-9]{3}. This subexpression matches either a six-digit or three-digit hexadecimal color code, which can optionally be preceded by a "#" symbol.

## Bracket Expressions
With in this regex the same bracketed expression is repeated twice, [a-f0-9]. A bracketed expression will accept any value in any of the ranges contained within it, in this example any letter from a to f in the alphabet and and number from 0 to 9 would be accepted.

## Character Classes
A character class is a set of characters enclosed in square brackets that specifies a pattern to match a single character from a range of possible characters.

The character class is represented by the expression [a-f0-9]. This character class matches a single character that is either a lowercase letter 'a' through 'f', a digit '0' through '9', or any character that falls within that range. The character class [a-f0-9] is used twice in the regex to match hexadecimal digits that make up the color code.

## OR Operator
An OR operator, is represented by the pipe symbol "|", it is used to match either one pattern or another. The OR operator allows you to provide multiple patterns, any one of which can be matched in a given string. In this regex the value we are looking to match must be either [a-f0-9]{6} or [a-f0-9]{3}.


## Flags
A flag is an optional setting that modifies the behavior of the regex pattern. Flags are added after the closing delimiter of a regex and are represented by letters, such as "i" for case-insensitive matching, "g" for global matching, "m" for multiline matching, etc. In the above Hex value its labeled with "i" at the end of the run. If this wasnt added it would change the hex value.

## Author
This was written by JAO https://github.com/Projectmayhem90