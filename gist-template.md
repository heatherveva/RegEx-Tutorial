# Matching a URL with Regex

Regular expressions, commonly referred to as regex, are highly functional code snippets that allow developers to validate user input information. Take, for instance, a properly formatted URL, phone number, IP address, or email address, while they all share common characteristics and follow patterns, they remain unique among users.

If you're unfamilar with regular expressions they may appear cryptic, even nonsensical, but with a little investigation regular expressions prove to be dynamic code snippets with consistent patterns.

The following tutorial will break down the regex used to match a URL. Through this break down, we will demystify the regular expression by disecting each component of the expression in detail.

## Summary

In this scenario, a developer is looking to validate a user input for a URL or web address. By determining the unique patterns contained within any URL, a developer can format and use and regex to ensure the user has correctly entered a URL. The regex to match a URL in Javascript appears below.

Matching a URL: `/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

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

The ^ and $ symbols are both considered anchors. These two characters mark the beginning and the end of a string value within a regular expression. In other words, anything inside of the ^ and $ notations is a string of characters to be validated, extracted, or replaced within a data set or program.

It is important to note that the string within these anchor tags can be in one of two formats. The first format would be an exact match string, for example, in our URL example above, we see the series of characters "https", this is considered an exact match. When the regex expression is put into use, it will only find strings containing the exact match to "https" in that position with the expression.

The second way the information between the anchor tags can be formatted is with ranges of characters. In our URL example, you'll notice character sets like "a-z". Instead of an exact match, this value designates a range of possible characters that could be contained within a URL in that position in the expression.

With that information, what can decipher within our regular expression? We know the regex will only find strings beginning with "https" and the characters within the range of a-z in two places later on in the string. Because regex is case sensitive, we can also determine that only lowercase letters are used in a URL.

### Quantifiers

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

I'm Heather Stevens, a burgeoning full stack developer. To view my recent projects and developer portflio, feel free to visit my GitHub profile.
