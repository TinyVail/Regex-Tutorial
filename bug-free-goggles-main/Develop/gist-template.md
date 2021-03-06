# Title (Explaining process of matching a "hex" value)

Introductory paragraph (replace this with your text)

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

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

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

### Anchors (^$)

The anchors in this regex, specifically `^` and `$`, denote the start and end of the line respectively.

### Quantifiers ({6}, {3})
simply put quantifiers specifies the number of instances of a character, character class, or group must be present in the selected input for a match to be properly found

{6} means that there must be exactly 6 characters within these requirements: [a-f0-9] 
{3} means that there must be exactly 3 characters within these requirements: [a-f0-9] 

### OR Operator (|)
The OR operator in this regex states that the string must contain either one of the capturing group alternatives directly before and directly after it, which in this case are:
[a-f0-9]{6} and [a-f0-9]{3}


### Character Classes [\w] -> any word [\d] -> any digit


### Flags (not in here, but one example is 'global')
Regular expressions can contain flags that directly affect the regex search, there are only 6 though:

I 
With this flag the search is case-insensitive: no difference between A and a (see the example below).

g 
With this flag the search looks for all matches, without it – only the first match is returned.

m
Multiline mode (covered in the chapter Multiline mode of anchors ^ $, flag "m").

s
Enables “dotall” mode, that allows a dot . to match newline character \n (covered in the chapter Character classes).

u
Enables full Unicode support. The flag enables correct processing of surrogate pairs. More about that in the chapter Unicode: flag "u" and class \p{...}.

y
“Sticky” mode: searching at the exact position in the text (covered in the chapter Sticky flag "y", searching at position)

(from: https://javascript.info/regexp-introduction)

P.S.- there are two different syntaxs, one in whcih uses qoutations (longer method) and the other uses backslashes (shorter method).

### Grouping and Capturing (())
There is a single capturing group defined here, inside the set of parenthesis. This allows the user to grab the hex without the numbersign proceeding it in the first capturing group

### Bracket Expressions [a-f]
A bracket expression can be one of two things: a simple matching list expression or it can be a non-matching list expression [a-f] would match the characters abcdef

It always consists of one or more expressions: collating elements, ordinary characters, equivalence classes, collating symbols, collating classes, character classes, or even range expressions

### Greedy and Lazy Match (All matches in here are greedy)
All matches in here are greedy meaning that they try to match as they possibly can instead of just matching the fewest times possible which would be lazy

### Boundaries https://www.regular-expressions.info/wordboundaries.html
They're are no boundaries in here but heres a simple explanation of boundaries (\b): \b allows you to perform a “whole words only” search using a regular expression in the form of \bword\b. A “word character” is a character that can be used to form words. All characters that are not “word characters” are “non-word characters” (https://www.regular-expressions.info/wordboundaries.html)

### Back-references (None here, but example is '\1')

Backreferences in a regex identifies a previously matched group of text and tries to search that same text again A great way to use backreferences is when you need to find repeated words through-out text.

### Look-ahead and Look-behind (None here, but example is (?=foo), which makes sure that the current text is preceeded by 'foo' but 'foo' itself is not part of the match)

## Author

Github Link --> https://github.com/TinyVail
