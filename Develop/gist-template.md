# Title (replace with your title)

Introductory paragraph (replace this with your text)



## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

const text = "Alice Johnson <alice.johnson@example.com>, Bob Lee <bob.lee@example.com>, \
Carla Davis <carla.davis@example.com>, user+label@example.com, invalid email.com";

// match all email addresses in the text
const regex = /(?<=^|\s)([a-z0-9._%+-]+)@([a-z0-9.-]+\.[a-z]{2,})(?=\s|$)/gi;

// find all matches in the text
const matches = [];
let match;
while ((match = regex.exec(text)) !== null) {
  const [_, username, domain] = match;
  matches.push({ username, domain });
}

// print the matches
console.log(matches);

This regular expression uses look-behind and look-ahead assertions to ensure that the email addresses are surrounded by whitespace or the beginning/end of the string. The group around the email address captures it for later use. This regex should match all valid email addresses in the string, and exclude any invalid email addresses such as "invalid email.com". The matches are then logged to the console.

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
Anchors (^ and $): matches the beginning and end of a string.
### Quantifiers
Quantifiers (+ and {2,}): matches one or more occurrences of the preceding character or group, or at least two occurrences of the preceding character or group, respectively.
### OR Operator
OR operator (|): matches either of the characters or groups separated by the operator.
### Character Classes
Character classes ([a-z0-9._%+-], [a-z]): matches any character in the specified set of characters.
### Flags
Flags (gi): "g" enables global matching, and "i" enables case-insensitive matching.
### Grouping and Capturing
Grouping and capturing (()): groups a series of characters or groups and captures the matched substring for later use.
### Bracket Expressions
Bracket expressions ([a-z0-9.-]): matches any character in the specified range of characters.
### Greedy and Lazy Match
Greedy and lazy match (+ and +?): matches as many characters as possible or as few characters as possible to satisfy the pattern.
### Boundaries
Boundaries (\b): matches the boundary between a word character (as defined by \w) and a non-word character (as defined by \W).
### Back-references
I did not use back-references in this example.
However, the back-reference \1 could be used to match a repeated character sequence, for example, to match a string that has two consecutive identical characters, you could use the following regex: const regex = /([a-z])\1/gi; <br />
This regex matches any lowercase character that is immediately followed by the same character, and captures the repeated character for later use using the back-reference \1.
### Look-ahead and Look-behind
Look-ahead ((?=)): matches the pattern only if it is followed by the specified pattern.
Look-behind ((?<=)): matches the pattern only if it is preceded by the specified pattern.
## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
