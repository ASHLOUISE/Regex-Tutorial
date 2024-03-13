# Demystifying Regular Expressions

Regular expressions, commonly known as regex, are powerful tools for pattern matching and text processing. They allow you to define patterns to search for and manipulate text efficiently. In this tutorial, we'll delve into the components of a basic regular expression to understand how it functions and how each part contributes to the pattern matching process.

## Summary

In this tutorial, we will dissect a basic regular expression that matches email addresses. We'll explain each component of the regex and its role in identifying valid email addresses. Here's the regex we'll be discussing:

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors
Anchors are special characters used to assert positions within the text. In our regex `\b` is a word boundary anchor. It ensures that the match occurs at the beginning or end of a word, thereby ensuring that the email address is not part of a larger word or phrase.

### Quantifiers
Quantifiers control the number of occurrences of a character or group in a regex pattern. In our regex, `+` and `{2,}` are quantifiers. `+` specifies that the preceding character set `[A-Za-z0-9._%+-]` should occur one or more times, allowing for multiple characters in the local and domain parts of the email address. `{2,}` specifies that the preceding character set `[A-Z|a-z]` should occur at least two or more times, ensuring the top-level domain (TLD) has a minimum length of two characters.

### Grouping Constructs
Grouping constructs allow you to treat multiple characters as a single unit. In our regex, there are no explicit grouping constructs, but you could use parentheses to group certain parts if you wanted to apply quantifiers or alternations to them as a whole.

### Bracket Expressions
Bracket expressions, also known as character classes, define a set of characters that can match at a particular position in the text. In our regex, `[A-Za-z0-9._%+-]` matches any alphanumeric character or special characters commonly found in email addresses, such as period (.), underscore (_), percent (%), plus (+), and hyphen (-).

### Character Classes
Character classes are similar to bracket expressions and define a set of characters that can match at a particular position in the text. In our regex, `[A-Z|a-z]` matches any uppercase or lowercase letter, ensuring that the TLD part of the email address consists of alphabetic characters.

### The OR Operator
The OR operator allows you to specify alternative matches. In our regex, the OR operator is represented by the pipe symbol (`|`) inside the character class `[A-Z|a-z]`. It allows either uppercase or lowercase letters to match for the TLD part of the email address.

### Flags
Flags are additional parameters that can be added to a regex pattern to modify its behavior. In our regex, there are no flags specified. However, common flags include `i` for case-insensitive matching or `g` for global matching (finding all matches rather than stopping after the first match).

### Character Escapes
Character escapes allow you to match characters with special meanings in regex as literals. In our regex, there are no character escapes used. However, if you needed to match a literal period (.) or at sign (@), you would precede it with a backslash () to escape its special meaning in regex.

## Author

Ashley Paluzzi
https://github.com/ASHLOUISE