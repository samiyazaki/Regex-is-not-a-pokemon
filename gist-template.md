# Utilizing Regex to Match Email Addresses

So you want to learn Regex in relation to matching email addresses? This is a great place to start. This gist will explain the regex components you will need to know to match email addresses. If you have any questions, please let me know by opening an issue on the GitHub repo or sending me an email at smsmiyazaki@gmail.com.

## Summary

I will be instructing you on ways in which to match email addresses using Regex, which is a universal way to help search for patterns in text. Regex is an extremely useful tool to employ as a developer and one you should at least be somewhat comfortable utilizing. The data we will be searching for in this tutorial will be `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`.

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
When developing Regular Expressions for email validation users can use two main anchors:
`^`: Which notes the beginning of the string
`$`: Which notes the end of the string
Thus when we are looking for a string that starts with a letter and ends with a letter, we can use the following regex: `/^[a-z]+$/`. This is to show that the string and search parameters are all of the valid characters between the `^` and `$` anchors.

### Quantifiers
When developing Regular Expressions for email validation users can use two types of quantifiers:
`+`: Which connects the previous character to the next character; or in this case, the users email name to the email service host and to the email service domain.
`{2,6}`: Which sets the minimum and maximum allowable number of characters that can be used in the email service domain.

### Grouping Constructs
In the provided data, there are three separate groups from which we can search for data:
The first group is delineated by the following characters `([a-z0-9_\.-]+)` and contains the email name. You can see that this group allows for any lowercase letter, any number from 0-9, an underscore, a period, and a dash. This group also allows for any combination of these characters and does not limit the length of the users email name.
The second group is delineated by the following characters `([\da-z\.-]+)`and contains the email service host. You can see that this group allows for any digit, any lowercase letter, a period and a dash. This group also allows for any combination of these characters and does not limit the length of the users email service host.
The third group is delineated by the following characters `([a-z\.]{2,6})` and contains the email service domain. You can see that this group allows for any lowercase letter and a period. This group also allows for any combination of these characters and limits the length of the users email service domain to a minimum of 2 characters and a maximum of 6 characters.

### Bracket Expressions
Bracket expressions are used to determine if a character is in a provided set of characters. The data is enclosed in square brackets and when referring to matching email addresses, the brackets help to determine if the characters are allowed in each group.
`[a-z0-9_\.-]`: This bracket expression allows for any lowercase letter, any number from 0-9, an underscore, a period, and a dash.
`[\da-z\.-]`: This bracket expression allows for any digit, any lowercase letter, a period and a dash.
`[a-z\.]`: This bracket expression allows for any lowercase letter and a period.

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

## References
https://www.rexegg.com/regex-anchors.html
https://coding-boot-camp.github.io/full-stack/computer-science/regex-tutorial
https://www.youtube.com/watch?v=rhzKDrUiJVk&ab_channel=WebDevSimplified
