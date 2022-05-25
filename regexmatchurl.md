# Matching a URL with Regex

Regular expressions, commonly referred to as regex, are highly functional code snippets which allow developers to validate user input information or run searches for character patterns. Take, for instance, a properly formatted URL, phone number, IP address, or email address, while they all share common characteristics and follow patterns, they remain unique among users.

If you're unfamiliar with regular expressions they may appear cryptic, even nonsensical, but with a little investigation regular expressions prove to be dynamic bits of code used to automate the process of matching character combinations in strings.

The following tutorial will break down the regex used to match a URL. Through this breakdown, we will demystify the regular expression by dissecting each of the expression’s components in detail.

## Summary

In this scenario, a developer is looking to validate a user input for a URL or web address. By determining the unique patterns contained within a typical URL, a developer can format and use a regular expression to ensure the user has correctly entered a URL and that that URL matches the expected criteria. The regex to match a URL in Javascript appears below.

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

The ^ and $ symbols are both anchors. These two characters mark the beginning and the end of a string value within a regular expression. In other words, anything inside of the caret and dollar sign notations are a string of characters to be validated, extracted, or searched against.

It is important to note that the string within these anchor tags can be in one of two formats. The first format would be an exact match string. In our example, we see the series of characters "https", this is considered an exact match. When the regex expression is put to use, it will only find strings containing the exact match to "https" in the specified position within the expression.

The second way the information between the anchor tags can be formatted is with ranges of characters. In our example, you'll notice character sets like "a-z". Instead of an exact match, this value designates a range of possible characters that could be contained within a URL in that position in the string.

It is also important to note here, regular expressions are case sensitive. In our match a URL regex, we notice only lower case letters noted throughout, this means our expression will only return URLs containing all lowercase letters.

### Quantifiers

Quantifiers set the minimum and maximum number of characters and patterns of a substring. Quantifiers are designated by curly brackets, asterisks, plus signs, or question marks.

The curly brackets ({}) can contain two, comma separated numbers. These two numbers note the minimum and maximum number of times the preceding pattern must occur.

The asterisk (\*) matches the preceding element zero or more times. An expression with this symbol after it never prevents a pattern from matching, it indicates that the preceding substring may or may not be present in the results.

The plus sign (+) indicates the regex will match one or more instances of the pattern directly preceding it.

The question mark (?) is looking to match the pattern zero or one time. This indicates that the string pattern may or may not appear in the results, but cannot appear more than once.

In our matching URL example, you’ll notice the two question marks at the beginning of the regex. This indicates that a URL will be matched with or without the string “https://”.

This small expression, ([a-z\.]{2,6}), towards the middle of the matching URL regex, notes that letters “a” through “z” followed by a period will be found two to six times in a valid search result.

### Grouping Constructs

Some regular expressions can be quite complex. Our matching a URL regex is a great example of a lengthy expression. In order to break down a complex regex and separate out smaller expressions within a regex, we can use grouping structures.

You'll notice three four sets of parentheticals. These four sets of parentheses separate out an individual substring of the regex, all of which can be pulled out and remembered. Grouping constructs make regular expressions more varied and gives a programmer an opportunity to pull substrings for future use.

### Bracket Expressions

Bracket expressions indicate a possible range of characters we'd like to match. Instead of searching for an exact character match, square brackets make regular expressions less rigid.

If an opening square bracket is followed with a caret symbol (^), the regex will exclude the characters following the carat from the search results.

In our matching URL expression [\da-z\.-] and [a-z\.] are included within the expression. This allows the regular expression to search for a range of characters. At its most basic level, you'll notice "a-z", the "-", or hyphen, notation indicating the expression will identify any match containing lower case letters "a" through "z".

### Character Classes

Character classes act as shorthand for including or excluding potentially large groups of characters. For example, the character class “/d” means all digits, the same as the bracket notation “[0-9]”. A backslash followed by a capital letter will perform the inverse match of its lower case counterpart.

The character class “.” encapsulates any character except a new line. In our matching a URL example, you notice the “.” are all escaped using the backslash notation. This is because our expression wants the “.” to be taken literally. In our case, the “.” is not being used as a character class.

In our example, we’ll find “/d” used to indicate the expression’s ability to match any single digit within its given substring.

### The OR Operator

The OR operator is one of many operators available for use in regex expressions. The OR operator is noted by the "|" symbol and indicates the regex will search for one character pattern or the other.

The matching a URL regex does not contain any OR operators.

### Flags

In regular expressions there are six optional flags. These flags can be used to define additional functions or limitations of the regex, including larger search mechanisms like global searching and case-insensitive searching.

If we look at our matching URL regex, we will not see any flags. This is because flags are used most commonly in advanced regular expressions, matching a URL, in our case, requires a less sweeping regex mechanism.

### Character Escapes

The backslash in regular expression escapes a character that may be interpreted literally. Essentially, because certain characters are used in regex to denote certain things, we need escape characters to indicate when we'd like to use those characters in their literal sense.

A great example can be found in our matching URL regex. In the first part of the string, the forward slashes following the "https" are escaped in order to note that we are looking to match two forward slashes exactly, rather than as they are used otherwise in regex expressions to terminate the pattern.

You will also notice the periods in our example regex are escaped with a preceding backslash. This is because we are asking the regex to validate actual "." within a URL. Without the escape character those period would be interpreted as a character class and would match any character except the new line character.

## Author

I'm Heather Stevens, a developer advocate who is excited to educate and assist software engineers on the usability and versatility of new technologies. I have a passion for continuous learning and of the power of trial and error.
