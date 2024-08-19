# Phone Number regular expression

The importance of inputting phone numbers into websites increase more and more as the years progress. Security has a big role in that fact but also SMS marketing is also an integral part of many businesses. During my job a few weeks back, I was working on updating a form that was created a while back and I spotted a bunch of weird characters and symbols. After researching, I realized it was a regular expression so I figured diagnosing a phone number regular expression would be perfect for this project.

## Summary

^(\+?\d{1,3}[-.\s]?)?(\(?\d{3}\)?[-.\s]?)?\d{3}[-.\s]?\d{4}$

Pasted above is the regex that will validate a phone number. Phone numbers come in a few different formats so this will get most possible scenarios.



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

Anchors match the starting and ending points of a string or line. In my example, 

- ^ is representing the beginning of a string 

- $ is representing the end of a string

### Quantifiers

Quantifiers are defined as metacharacters that specify how many times the previous character or group should be matched. In the example,

- The \+ in \+? means that we are looking for the literal character "+" and the ? quanitifer is saying that we are lloking for 0 or 1 times of it occuring.

- We also see {1,3} which is matching between 1 to 3 occurences of whatever is in front of it. In this case the entire expression is \d{1,3}, meaning 1 to 3 digits.

- We also see a {3} which is matching exactly 3 occurences.

- We also see a {4} which is matching exactly 4 occurences.

### Grouping Constructs

Grouping Constructs are used to capture different parts of the regular expression so that the groups can be referred to at a later time. This is used twice in my example, 

- (\+?\d{1,3}[-.\s]?)? This is mainly used because of the question mark meta character at the end which signifies this entire first group is optional

- (\(?\d{3}\)?[-.\s]?)? This is used in more or less the same way in the second group

- NOTE: group 0 is known as the entire expression, ^(\+?\d{1,3}[-.\s]?)?(\(?\d{3}\)?[-.\s]?)?\d{3}[-.\s]?\d{4}$

### Bracket Expressions

Bracket expressions are used to specify a set of characters that can be matched at that position. THis is used three times but its the same expression, 

- [-.\s] Meaning that we are matching the literal symbol "-", or the literal symbol ".", or a blank space which is represented as "\s".

### Character Classes

Character classes match specific characters that are defined in the expression. THis is used only twice in my example, 

- \d Meaning any digit equivalent to 0-9

- \s meaning any whitespace character

### The OR Operator

This is used in alternation cases and in my example there is no instances of it. The OR operator is used like so, 

- (a|b|c) Meaning a OR b OR c

### Flags

Flags are used to modify how the expression is interpreted and are found at the end of the expression. There are no flags being used in my expression. Some examples might be, 

- /hello/i Meaning that this would ignore case sensitive spellings of hello. This is because of the i at the end.


### Character Escapes

Character escapes are used to indicate that some characters should be treated a literals. Some examples are,

- \+ Meaning the + is a literal character and not a quantifier which it usually is used as.

- \( and \) Meaning both the parathesis are used literally and not for grouping purposes

## Author

My name is Michael Drag and I an aspiring developer. My GitHub link is https://github.com/mbdrag3
